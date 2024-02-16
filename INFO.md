## frame mod

- p enum Request
    into_owned
    function_code
    
- p struct SlaveRequest
    into_owned

- p enum Response
    function_code

- p enum Exception

- p struct ExceptionResponse

- pc struct RequestPdu(Request)

- pc struct ResponsePdu(Result<Response, ExceptionResponse>)

## frame tcp

- pc struct Header
- p struct RequestAdu
    + pc Header
    + pc RequestPdu
    + pc disconnect
- pc struct ResponseAdu
    + Header
    + ResponsePdu