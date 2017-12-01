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
