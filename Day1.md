# Day1 刷题记录

## 今日刷题内容
- 二分查找
- 移除元素
- 反转链表

## 题目总结
- 二分查找：注意区间边界 [left, right]
- 移除元素：双指针技巧
- 反转链表：需要掌握链表基本操作

### 示例（Python）：
```markdown
```python
class Solution:
    def search(self, nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = left + (right - left) // 2
            if nums[mid] == target:
                return mid
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return -1
