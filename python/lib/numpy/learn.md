**Why NumPy?**

```python
import random
import statistics
import numpy as np
from datetime import datetime

nums = [random.randint(a=0, b=1_000_000) for _ in range(1_000_000)]

start_time = datetime.now()
mean = statistics.mean(data=nums)
end_time = datetime.now()
duration = end_time - start_time
print("by statistics duration", duration)

start_time = datetime.now()
mean = np.mean(nums)
end_time = datetime.now()
duration = end_time - start_time
print("by np duration", duration)

# My results
# [terminal] python python/lib/numpy/main.py
# [terminal] by statistics duration 0:00:00.109326
# [terminal] by np duration 0:00:00.033918
```
