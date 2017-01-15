# Fractalfy
Wrapper for Fractal

## Fractal methods
Use Fractalfy class or FractalfyController

Return collection
```php
$users = Users::all();
return $this->fractal
    ->collection($users, new UserTransformer)
    ->get();
```

Return resource with pagination
```php
$users = Users::all();
return $this->fractal
    ->paginate($dashboards, new DashboardTransformer)
    ->get();
```

## Fractalfy Helpers
Use Fractalfy Helpers

Popular
```php
return $this->respondOK();
return $this->respondNotFound();
return $this->respondUnauthorized();
return $this->respondUnprocessable();
return $this->respondBadRequest();
return $this->respondWithSuccess(200); //any success code
return $this->respondWithError(400); //any success code
```

Other
```php
return $this->respondOK($message); //pass message to respond
return $this->setMessage($message)->respondOK();
return $this->setMessage($message)->setStatusCode($statuscode)->respondWithSuccess(); 
return $this->setMessage($message)->setStatusCode($statuscode)->respondWithError(); 
```



