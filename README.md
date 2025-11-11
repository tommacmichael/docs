# Cyclemate API Documentation

This directory contains the Mintlify-powered API documentation for Cyclemate's public APIs.

## Documentation Structure

### Introduction
- `api-reference/introduction.mdx` - Overview, authentication, and key features

### Events API
- `api-reference/events/nearby.mdx` - Find cycling events, group rides, and leisure routes
- `api-reference/events/detail.mdx` - Get detailed event information

### Bikes API
- `api-reference/bikes/nearby.mdx` - Real-time bike-share availability (docked and dockless)

### Routing API
- `api-reference/routing/directions.mdx` - Turn-by-turn directions with optional super-safe routing
- `api-reference/routing/multimodal.mdx` - Multi-modal routes with bike-share integration

### Search API
- `api-reference/search/mapbox-search.mdx` - Place search with bike-friendly enrichment

### Location API
- `api-reference/location/nearby-areas.mdx` - Find nearby areas/neighborhoods

### Analytics API
- `api-reference/analytics/qr-track.mdx` - QR code scan tracking

## Configuration

The documentation is configured via `docs.json`, which defines:
- Navigation structure
- Theme and colors
- Logo and branding

## Running Locally

To preview the documentation locally:

```bash
# Install Mintlify CLI
npm i -g mintlify

# Navigate to docs directory
cd docs

# Start the dev server
mintlify dev
```

The documentation will be available at `http://localhost:3000`.

## Deployment

The documentation can be deployed to Mintlify's hosting platform or self-hosted using their enterprise options.

## API Endpoints Documented

All endpoints require Auth0 authentication:

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/events/nearby/` | Find nearby events and leisure routes |
| GET | `/bikes/nearby/` | Find available bikes (docked/dockless) |
| POST | `/directions/` | Get turn-by-turn directions |
| POST | `/multi-modal/` | Get multi-modal bike-share routes |

## Notes

- All coordinates use `[longitude, latitude]` format (GeoJSON standard)
- Distances are in meters or miles as specified per endpoint
- Responses are JSON format
- Auth0 bearer token required for all requests
- Documentation follows Mintlify best practices with interactive examples
