# Request-Response Pattern
Remote request with async response:

| on:command	| →	| do:request GET:JSON | 
|---|---|---|
> Action ← response ••• https://www.company.com/actions/response.json
> 
> | on:command	| →	| do:say | 
> |---|---|---|
>> "Async Response Reaction" 🗣

Hint: REST is stateless, therefore handle state on client.