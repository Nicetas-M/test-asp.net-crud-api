### A test project created for educational purposes

---


If `dotnet ef` does not working:
`dotnet tool install --global dotnet-ef`

```
dotnet build
dotnet ef migrations init -s ./BookStore.API/ -p ./BookStore.DataAccess/
dotnet ef database update -s ./BookStore.API/ -p ./BookStore.DataAccess/
dotnet run --project ./BookStore.API/
```

API Endpoints:
- GET {uri}/books/
- POST {uri}/books/{id}
	- "title": string|max:250,
	- "description": string,
	- "price": decimal
- PUT {uri}/books/{id}
	- "title": string|max:250,
	- "description": string,
	- "price": decimal
- DELETE {uri}/books/{id}
