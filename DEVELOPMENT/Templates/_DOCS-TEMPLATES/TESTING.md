# [ PROJECT NAME ] - Testing Guide
*Version: 1.0.0*

## Test Types

### Unit Tests
```typescript
// Component test example
describe('Component', () => {
  it('renders correctly', () => {
    const { getByText } = render(<Component />)
    expect(getByText('Hello')).toBeInTheDocument()
  })
})
```

### Integration Tests
```typescript
// API test example
describe('API', () => {
  it('returns data', async () => {
    const response = await request(app).get('/api/data')
    expect(response.status).toBe(200)
  })
})
```

### E2E Tests
```typescript
// E2E test example
describe('App', () => {
  it('completes user flow', () => {
    cy.visit('/')
    cy.get('button').click()
    cy.url().should('include', '/dashboard')
  })
})
```

## Test Commands
```bash
# Run all tests
npm test

# Run unit tests
npm run test:unit

# Run integration tests
npm run test:int

# Run E2E tests
npm run test:e2e

# Generate coverage
npm run test:coverage
```

## Test Structure
```
tests/
├── unit/
│   ├── components/
│   └── utils/
├── integration/
│   ├── api/
│   └── db/
└── e2e/
    ├── flows/
    └── pages/
```

## Coverage Targets
- Statements: 80%
- Branches: 80%
- Functions: 80%
- Lines: 80%

## CI Pipeline
```yaml
test:
  stage: test
  script:
    - npm test
    - npm run test:coverage
