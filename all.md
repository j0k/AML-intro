#

## naming

```
self.mongo_host, self.mongo_port = self.config['mongoURI'].split(':')
self.client = MongoClient(self.mongo_host, int(self.mongo_port))
```
the same as
```
host, port <= self.config['mongoURI'].split(':'):
  self.client = MongoClient(host, int(port))
```
the same as
```
self.client = MongoClient( host, port:int ) <= self.config['mongoURI'].split(':'))
```
the same as
```
self.client = MongoClient( host, port ) <= [:string, :int] <= self.config['mongoURI'].split(':'))
```


## file format (FF)

let's think about something like JSON

it will be cool to dump FF object to file and it will be consistent . You can't do smth in JSON course you need end array with ']' : [{}, {}, {}]
