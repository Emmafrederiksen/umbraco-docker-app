# Umbraco Docker App

A containerized Umbraco CMS project using .NET and SQL Server, configured with Docker and Docker Compose.

---

## Tech Stack

* Umbraco CMS
* .NET 10
* Microsoft SQL Server (Docker)
* Docker & Docker Compose
* Docker Hub (multi-platform image)
* GitHub (version control)

---

## Features

* Containerized Umbraco application
* SQL Server running in Docker
* Multi-platform Docker image (amd64 + arm64)
* Environment variables for secure configuration
* Ready for local development and deployment

---

## Run with Docker Compose

Start the database container:

```bash
docker-compose up -d
```

Run the Umbraco application locally:

```bash
dotnet run
```

---

## Access

* Frontend: [https://localhost:xxxx](https://localhost:xxxx)
* Backoffice: [https://localhost:xxxx/umbraco](https://localhost:xxxx/umbraco)

*(Replace port with the one shown in terminal)*

---

## Environment Variables

Create a `.env` file in the root:

```env
DB_PASSWORD=your_password_here
```

---

## 🐳 Docker Image

The application is available as a multi-platform Docker image:

```bash
docker pull emma4147/umbraco-app:1.1
```

Supports:

* linux/amd64
* linux/arm64

---

## Build Image (Multi-platform)

```bash
docker buildx build --platform linux/amd64,linux/arm64 -t emma4147/umbraco-app:1.1 --push .
```

---

## Project Structure

```text
.
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
├── .gitignore
├── Program.cs
├── umbraco-sql.csproj
├── Views/
└── wwwroot/
```

---

## Notes

* Database runs in a separate Docker container
* App and DB are decoupled (best practice)
* Secrets are not included in the repository

---

## Author

Emma Øhlers Frederiksen
