### finatra
---

https://github.com/twitter/finatra

```
```

```ruby
import com.twitter.finatra.http.-
@Singleton
class ExampleController extends Controller {
  get("/") { request: Request =>
    "<h1>Hello!</h1>"
  }
}

import com.twitter.finatra.http.-
class ExampleServer extends HttpServer {
  override def configureHttp(router: HttpRouter): Unit = {
    router
      .filter[CommonFilters]
      .add[ExampleController]
  }
}

import com.twitter.finatra.thrift.-
@Singleton
class ExampleThriftController
  extends Controller
  with MyThriftService.BaseServiceIface {
  
  override val myFunction = handle(MyFunction) { args: MyFunction.Args =>
  }
}



```

```
```

