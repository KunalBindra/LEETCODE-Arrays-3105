# LEETCODE-Arrays-3105
### Example Input:
```java
nums = [1, 2, 2, 3, 4, 1, 2, 3, 1]
```

### Initialization:
- `n = nums.length = 9`
- `result = 1`
- `inc = 1` (to track the length of the current increasing subarray)
- `dec = 1` (to track the length of the current decreasing subarray)

---

### Iteration Details:
#### Iteration 1 (`j = 1`):
- `nums[1] = 2`, `nums[0] = 1`
- Condition: `nums[j] > nums[j-1]` (True)
  - `inc = 2`, `dec = 1`
  - `result = max(result, inc) = max(1, 2) = 2`

#### Iteration 2 (`j = 2`):
- `nums[2] = 2`, `nums[1] = 2`
- Condition: `nums[j] > nums[j-1]` (False) and `nums[j-1] > nums[j]` (False)
  - Reset: `inc = 1`, `dec = 1`

#### Iteration 3 (`j = 3`):
- `nums[3] = 3`, `nums[2] = 2`
- Condition: `nums[j] > nums[j-1]` (True)
  - `inc = 2`, `dec = 1`
  - `result = max(result, inc) = max(2, 2) = 2`

#### Iteration 4 (`j = 4`):
- `nums[4] = 4`, `nums[3] = 3`
- Condition: `nums[j] > nums[j-1]` (True)
  - `inc = 3`, `dec = 1`
  - `result = max(result, inc) = max(2, 3) = 3`

#### Iteration 5 (`j = 5`):
- `nums[5] = 1`, `nums[4] = 4`
- Condition: `nums[j-1] > nums[j]` (True)
  - `dec = 2`, `inc = 1`
  - `result = max(result, dec) = max(3, 2) = 3`

#### Iteration 6 (`j = 6`):
- `nums[6] = 2`, `nums[5] = 1`
- Condition: `nums[j] > nums[j-1]` (True)
  - `inc = 2`, `dec = 1`
  - `result = max(result, inc) = max(3, 2) = 3`

#### Iteration 7 (`j = 7`):
- `nums[7] = 3`, `nums[6] = 2`
- Condition: `nums[j] > nums[j-1]` (True)
  - `inc = 3`, `dec = 1`
  - `result = max(result, inc) = max(3, 3) = 3`

#### Iteration 8 (`j = 8`):
- `nums[8] = 1`, `nums[7] = 3`
- Condition: `nums[j-1] > nums[j]` (True)
  - `dec = 2`, `inc = 1`
  - `result = max(result, dec) = max(3, 2) = 3`

---

### Final Result:
The length of the longest monotonic subarray is:
```java
result = 3
```
