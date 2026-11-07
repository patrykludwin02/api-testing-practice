# API Testing Practice

Manual API testing practice in Postman. I test two public practice APIs and document each test case with the request, the expected result, the actual result and a screenshot.

## APIs tested

| API | What it is | Test cases |
|---|---|---|
| [JSONPlaceholder](https://jsonplaceholder.typicode.com) | Fake REST API for posts, users and comments | [test-cases.md](test-cases.md) |
| [Restful-Booker](https://restful-booker.herokuapp.com) | Booking API with authentication | [test-cases-restful-booker.md](test-cases-restful-booker.md) |

## What is covered

- HTTP methods: GET, POST, PUT, PATCH, DELETE
- Status codes and response bodies
- Negative cases (non-existent resource, empty body, missing authorization)
- Authentication: requesting a token and using Basic Auth

## Repository structure

```
.
├── README.md
├── test-cases.md                    JSONPlaceholder test cases
├── test-cases-restful-booker.md     Restful-Booker test cases
└── images/                          Postman screenshots used in the test cases
```

## How to repeat the tests

1. Install [Postman](https://www.postman.com/downloads/).
2. Create the requests described in each test case (method, URL and body).
3. Send them and compare the responses with the expected results.

## Notes

- Both APIs are public practice services. JSONPlaceholder only simulates writes, and Restful-Booker data is shared and reset periodically.
- Some findings are documented in the test cases, for example Restful-Booker returns 200 on create and 201 on delete.

## Next steps
- Automate the same scenarios in Python with `requests` and `pytest`