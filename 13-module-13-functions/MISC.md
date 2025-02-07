```python

>>> import time
>>> import random
>>>
>>> names = ["Sagar", "Qadeer", "Deepak", "Kamlesh"]
>>> subjects = ["AI", "UI", "ICT","ML"]
>>>
>>>
>>> def people_list(num_of_people):
...     results = []
...     for i in range(num_of_people):
...             person = { 'id': i,
...                     'name':random.choice(names),
...                     'subject':random.choice(subjects)
...                     }
...             results.append(person)
...     return results
...
>>> people_list(2)
[{'id': 0, 'name': 'Kamlesh', 'subject': 'ICT'}, {'id': 1, 'name': 'Sagar', 'subject': 'ICT'}]
>>>
>>>
>>> def people_generator(num_of_people):
...     for i in range(num_people):
...             person = { 'id':i,
...                     'name':random.choice(names),
...                     'subject':random.choice(subjects)
...                     }
...     yield person
...
>>>
>>>
>>>
>>>
>>> start = time.time()
>>> p = people_list(10000000)
>>> end = time.time()
>>> end - start
28.782392024993896
>>>
>>>
>>>
>>> start = time.time()
>>> p = people_generator(10000000)
>>> end = time.time()
>>> end - start
2.3284177780151367

```