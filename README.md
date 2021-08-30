# 367. Valid Perfect Square

Using BinarySearch:

```swift
class Solution {
    func isPerfectSquare(_ num: Int) -> Bool {
        guard num >= 2 else { return true }
        
        var left = 2
        var right = num / 2
        
        while left <= right {
            let pivot = (left + right) / 2
            let pivotSquare = pivot * pivot
            if pivotSquare == num {
                return true
            }
            
            if pivotSquare > num {
                right = pivot - 1
            } else if pivotSquare < num {
                left = pivot + 1
            }
        }
        
        return false
    }
}
```

{% hint style="info" %}
Time complexity: O\(log n\)
{% endhint %}

{% hint style="info" %}
Space complexity: O\(1\)
{% endhint %}





