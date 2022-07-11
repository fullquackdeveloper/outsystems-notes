# Development and delivery at scale

## Team structure and architecture

* independent, isolated teams
* increases delivery speed
* independent development
* independent delivery
* independently aligned with business goals
* loosely coupled architecture

### Domain-driven design

* scalability
* resilience
* maintainability
* less dependencies between development teams
* business domain can evolve at different speeds

### Team structure

A cross-functional team is fully independent and autonomous to promote code changes from development to production.

### Ownership and governance

Only one team is the owner of each software domain.

## Collaboration

### Small batch approach

* decompose complex solutions into smaller components
* deployed incrementally and tested independently
* tested and released quickly
* lowers the risk in development
* accelerates the release rate 
* realize business value faster
* enhance productivity
* fewer errors

### Trunk-based development patterns

* API/UI versioning
* Feature toggles
* Branching by abstraction

## Quality validations

### Code quality

* TrueChange
* Architecture dashboard
* Static-code analysis (automated)
* Code review (manual)

### Functional quality

* Automated testing

## Production hotfixes

### Release/deployment pace

### Application criticality

### Hotfix process with pre-production environment

* Same environment version
* Mimic prod environment
* Simulate deployment
* Production-like data
* Smoke tests
* Load and performance tests
* Necessary validations (manual tests, regression tests)
* Correct governance
* Merge fixes back to start of pipeline