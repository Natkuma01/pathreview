## Solution plan

**Issue:** API reference doc is missing the `POST /profiles` request body schema #89 (https://github.com/ascherj/pathreview/issues/89)

### Understand
The documentation in `docs/API.md` does not explain request body schemas. Users cannot see what parameters to send when calling `POST /profiles` or `POST /reviews`. We must add tables and examples for these request bodies.

### Map
The following files are involved:
- [API.md](file:///Users/nataliechan/Desktop/codePath/ai210/pathreview/docs/API.md) (The documentation file to edit)
- [profiles.py](file:///Users/nataliechan/Desktop/codePath/ai210/pathreview/api/routes/profiles.py) (Defines profiles endpoint parameters)
- [reviews.py](file:///Users/nataliechan/Desktop/codePath/ai210/pathreview/api/routes/reviews.py) (Defines reviews endpoint parameters)

### Plan
1. Check the request parameters for profile creation in `api/routes/profiles.py`.
2. Check the request schemas for review creation in `api/routes/reviews.py`.
3. Add multipart request body table and example to `docs/API.md` for `POST /profiles`.
4. Add JSON request body table and example to `docs/API.md` for `POST /reviews`.

### Inputs & outputs
- Input: Route parameters and Pydantic schemas in code.
- Output: Tables and examples in `docs/API.md`.

### Risks & unknowns
- The Pydantic schemas or route parameters could change in future commits. We must keep documentation in sync.

### Edge cases
- `POST /profiles` uses `multipart/form-data` with a file payload.
- `POST /reviews` uses `application/json` with a JSON payload.
