# Request-Response Pattern

The Request-Response Pattern is a method of communicating with remote services through non-blocking asynchronous communication. This pattern is commonly used to request media assets such as images, audio files, video streams, or 3D models, as well as scripts such as additional ECA rules. Because of the temporal decoupling of request and response, an event is required to signal the arrival of the received data from the server. This allows an ECA rule to handle the result as soon as it is available.

## ECA Diagram

Remote request with async response:

| on:command	| →	| do:request GET:JSON | 
|---|---|---|
> Action ← response ••• https://www.company.com/actions/response.json
> 
> | on:command	| →	| do:say | 
> |---|---|---|
>> "Just received response from a request." 🗣

Hint: REST is stateless, therefore handle state on client.
