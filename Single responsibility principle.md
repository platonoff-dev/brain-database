### Single responsibility principle
Example:
```python
class Customer:
	def add(self, client: Connection) -> None:
		"""
		Insert customer in database
		"""
		client.Add();
		with open("logs.txt") as log_file:
			log_file.write("Customer created")
		
```

This is a bad example because if we want to change filename or destination of logs (HTTP/UDP server) we need to change code.

```python
class Customer:
	def __init__(self, logger: Logger) -> None:
		self.logger = logger
	
	def add(self, client: Connection) -> None:
		"""
		Insert customer in database
		"""
		client.Add();
		self.logger.info("Customer created")

customer = Customer(FileLoger("logs.txt"))
```
This example is way better.