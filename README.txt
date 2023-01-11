The code business logic was okay, but in terms of readability and maintainability there are so much things needs to adjust.
Below are the list of refactoring that can be apply to make the code more readable and to maintain


# Controller
1. make use of laravel Helpers like auth(), response()
2. use route model binding like on show() method of controller
3. always validate request by making use of custom request class for validation
4. instead of plain array, use API Resource class in returning response on controller methods
5. Alway stick to 5 API resource method (index, show, store, update and delete)
6. Create Service or Action class to move other logic there, controller needs to have single responsibility which is consuming other class to output the needed response

# Refactoring
1. dont acceing the env value (env()) directly instead use config file (config())
2. instead of plain curl, use the HTTP client of the laravel to maximize other feature
3. instead of static class like TeHelper.php, use the facades patter to make it more flexible and readable
4. instead of doing query builder on different area of the codes, you can use QueryObjects or put it on model as scope queries


# Readability Purposes:
1. inside if condition use fluent interface instead of using conditional operators
2. Create Service or Action class to move other logic there and to make the logic reusable
3. make the code more readable by using fluent interface.
4. Create DataTransferObject or Plain Old PHP Object to pass parameters on methods if the parameters are more than 3
5. for alot of cases on the switch statement, you can use array (key => value pair) or use the latest match() function
6. always type hint parameters and function / method return value
7. Don't ever use magic number or plain string on assigning value, instead use contants or enums to have centralized placed for those values
