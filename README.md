# graphite_demo

### Project features
1. Create a new class Person with the Name attribute in a file called "person.py"
```python
class Person:
    def __init__(self, name):
        self.name = name
```

Now, create a new stacked branch with `gt bc {branch_name} -a -m "{commit message}"`

2. Create a new file "helpers.py" with a function that takes the name as an input

```python
def get_name():
    return input("give name pls: ")
```

create another stacked branch with `gt bc {branch_name} -a -m "{commit message}"`

submit your branches with `gt stack submit`

3. check out your previous branch with `gt branch prev` and update the Person class
```python
class Person:
    def __init__(self, name):
        self.name = name.lower()
```

update this branch with `gt commit create -a -m "{commit message}"`

re-submit your stack with these changes with `gt stack submit`

4. Integrate these features to print "Hello, NAME" when given a name from the cli

```python
from src.helpers import get_name
from src.person import Person

def main():
    name = get_name()
    person = Person(name=name)
    print("hello {}".format(person.name))

if __name__ == "__main__":
    main()

```

create another stacked branch with `gt bc {branch_name} -a -m "{commit message}"`

submit your branches with `gt stack submit`