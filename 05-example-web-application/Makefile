
DATABASE_URL:=postgres://postgres:Tekobou22080825@@localhost:5433/postgres

.PHONY: run-postgres
run-postgres:
	@echo Starting postgres container
	-docker run \
		-e POSTGRES_PASSWORD=Tekobou22080825@ \
		-v pgdata:/var/lib/postgresql/data \
		-p 5433:5432 \
		postgres:15.1-alpine

.PHONY: run-api-node
run-api-node:
	@echo Starting node api
	cd api-node && powershell.exe -Command "$$env:DATABASE_URL='$(DATABASE_URL)'; npm run dev "\
		

.PHONY: run-api-golang
run-api-golang:
	@echo Starting golang api
	cd api-golang && \
		powershell.exe -Command "$$env:DATABASE_URL='$(DATABASE_URL)'; go run main.go"\
		


.PHONY: run-client-react
run-client-react:
	@echo Starting react client
	cd client-react && \
		npm run dev
