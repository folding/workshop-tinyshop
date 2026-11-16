## TinyShop

<!-- Add./Replace Instructions here -->
- Use inline css in the same razor file, keep ui simple as possible, nothing custom

## Frontend
- The storefront is the `Store` Blazor Web App, built with .NET 10 Razor components and Interactive Server rendering.
- Pages and layouts live under `Store/Components`; the products page is currently a placeholder, so keep its implementation consistent with the existing simple UI.
- Use `Store/Services/ProductService` to communicate with the products backend rather than calling its API directly from components.
- Product data is shared through the `DataEntities` project. Product images use the configured `ImagePrefix` as described below.

## Backend
- The `Products` project is a .NET 10 ASP.NET Core minimal API. Product endpoints are mapped from `Products/Endpoints/ProductEndpoints` under `/api/Product` and provide CRUD operations.
- Product persistence currently uses Entity Framework Core's in-memory provider and seeds sample products at startup; do not assume a durable database.
- `DataEntities/Product` is the shared product contract. The `TinyShop.AppHost` Aspire project starts the `Store` and `Products` projects and provides their service reference.

## Misc
- To display an image you will always need to use `ImagePrefix` in the web front end which comes from the Configuration["ImagePrefix"] which isc @inject IConfiguration Configuration 
- Ignore all *.md files code in the **lab** folder when making code suggestions.
