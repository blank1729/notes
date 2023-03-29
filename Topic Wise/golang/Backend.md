



### Routing

- [go - A good way to build a subrouter with net/http - Stack Overflow](https://stackoverflow.com/questions/60841156/a-good-way-to-build-a-subrouter-with-net-http)
	```go
type UserRouter struct {
    cfg *Config

    // prefix is the path prefix for the user handlers. Use this
    // value to construct paths to other user handlers.
    prefix string 
}

// RegisterUserHandler adds the user handlers to mux using the
// specified path prefix.
func RegisterUserHandler(cfg *Config, prefix string, mux *http.ServeMux)  {
    u := &UserRouter{cfg: cfg, prefix: prefix}
    mux.HandleFunc(prefix+"/create", u.Create)
    mux.HandleFunc(prefix+"/delete", u.Delete)
}

func main() {
    mux := http.NewServeMux()
    cfg := &Config{nil /* Describes settings such as PostgreSQL. */}
    RegisterUserHandler(cfg, "/user", mux)
    log.Fatal(http.ListenAndServe(":8080", mux))
}
```