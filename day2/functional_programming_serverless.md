## Functional and event-driven programming in a serverless world?
_Serverless Track_

_Kacper Walanus, platformOS_

Analyzing Google trends one can see that docker popularity influenced popularity of micro services and SOLID concept.
It's developer dream to write a code and see it running without containers etc, thus lambda sounds like a proper magic.

Is serverless going to change the way we design our apps? Function-centric approach is a powerful way to create services. This design does not require to go serverless but definitely will help in case of decision.

#### Function should be:
- easy to call via WebAPI (ex. `/api/invite-user?user_id={user_id}`)
- easy to extract to a micro service (would it be easy to write it in another language? How many deps is required?)
- produce events (leave traceback somewhere, execute other function, put event in queue)
- run in the background (possible to call functions asynchronously, do not block resources etc)
- idempotent (no side effects)

#### Demo
Chaining the function could use template language to get values from previous steps (like in Airflow).
Chaining functions has quite monadic behavior on error. One can create lambdas to invoke lambdas.

#### Implementation hints
Input validations and authentication are integral part. Whenever  a function is execute it should validate
input and access. 
