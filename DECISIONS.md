# Design Decisions

> Update these notes to match the implementation you actually build and understand.

## API structure
- Keep HTTP endpoints thin: validate inputs, call the relevant logic, and return the documented response.
- Follow the exact route names, status codes, and schemas in the supplied OpenAPI contract.

## Data model
- Use the collection names and document fields required by the supplied data model.
- Store timestamps consistently; follow the specification's timezone rules.
- Add indexes only where justified by the required query patterns.

## Business rules
- Implement punch-in/punch-out restrictions exactly as described in the problem statement.
- Record manual corrections in an audit trail, including the actor, timestamp, and before/after values if required by the contract.

## Analytics
- Implement the required analytics using MongoDB aggregation pipelines, not by loading all documents into Python and calculating results there.
- Explain each pipeline's filtering, grouping, and output shape.

## Error handling and validation
- Return the documented HTTP status codes and error format.
- Validate input at the API boundary and avoid exposing secrets or internal stack traces.

## Trade-offs and limitations
- Explain any choices or incomplete work here.
