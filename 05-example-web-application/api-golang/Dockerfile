FROM golang:1.19-buster as build

WORKDIR /app

RUN useradd -u 1001 nonroot

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build \
  -ldflags="-linkmode external -extldflags -static" \
  -tags netgo \
  -o api-golang

# Use separate stage for deployable image
FROM scratch

# Set gin mode
ENV GIN_MODE=release


# Copy the binary from the build stage
COPY --from=build /etc/passwd /etc/passwd

COPY --from=build /app/api-golang api-golang

USER nonroot

# Indicate expected port
EXPOSE 8080

CMD ["/api-golang"]