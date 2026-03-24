# Proof of Concept - Elderly Care Alert System

## Scope
- App category: Business & Commerce
- Entity model: Elderly Care Order
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Client Name: `client_name` (text)
- Estimated Value: `estimated_value` (number)
- Delivery Notes: `delivery_notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"quoted","payload":{"client_name":"Demo value","estimated_value":12,"delivery_notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 30
- Generated UTC: 2026-03-24T15:52:21.953483+00:00
- Status: Phase-2 complete
