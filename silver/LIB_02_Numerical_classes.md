Numeric is the class from which all higher-level numeric classes should inherit.

Numeric allows instantiation of heap-allocated objects.
Other core numeric classes such as Integer are implemented as immediates, which means that each Integer is a single immutable object which is always passed by value.

```ruby
a = 1
1.object_id == a.object_id   #=> true
```

Class Numeric:
- Inherits from class Object.
- Includes module Comparable.

### Querying

#### finite?
Returns true unless self is infinite or not a number.

#### infinite?
Returns -1, nil or +1, depending on whether self is -Infinity<tt>, finite, or <tt>+Infinity.

#### integer?


#### negative?

#### nonzero?

#### positive?

#### real?
Returns true if num is a real number (i.e. not Complex).

#### zero?
Returns true if num has a zero value.


### Comparing

#### <=>
- -1 if self is less than the given value.
- 0 if self is equal to the given value.
- 1 if self is greater than the given value.
- nil if self and the given value are not comparable.

#### eql?
Returns whether self and the given value have the same value and type.

### Converting
### 1. **`-@` (Negation)**
Trả về giá trị âm của `self`.

```ruby
num = 5
puts -num  # Output: -5
```

---

### 2. **`abs` (hoặc `magnitude`)**
Trả về giá trị tuyệt đối của `self`.

```ruby
num = -10
puts num.abs  # Output: 10
```

---

### 3. **`abs2`**
Trả về bình phương của `self`.

```ruby
num = 4
puts num.abs2  # Output: 16
```

---

### 4. **`ceil`**
Trả về số nguyên nhỏ nhất lớn hơn hoặc bằng `self`, với độ chính xác được chỉ định.

```ruby
num = 3.14
puts num.ceil  # Output: 4

num = 2.022
puts num.ceil(1)  # Output: 2.1 (làm tròn đến 1 chữ số thập phân)
```

---

### 5. **`div`**
Trả về kết quả của phép chia `self` cho một giá trị và chuyển đổi thành số nguyên.

```ruby
num = 10
puts num.div(3)  # Output: 3 (10 / 3 = 3.333..., làm tròn xuống thành 3)
```

---

### 6. **`floor`**
Trả về số nguyên lớn nhất nhỏ hơn hoặc bằng `self`, với độ chính xác được chỉ định.

```ruby
num = 3.99
puts num.floor  # Output: 3

num = 2.022
puts num.floor(1)  # Output: 2.0 (làm tròn đến 1 chữ số thập phân)
```

---

### 7. **`round`**
Trả về giá trị của `self` được làm tròn đến giá trị gần nhất với độ chính xác được chỉ định.

```ruby
num = 3.14159
puts num.round(2)  # Output: 3.14 (làm tròn đến 2 chữ số thập phân)
```

---

### 8. **`to_int`**
Trả về biểu diễn số nguyên của `self`, cắt bỏ phần thập phân nếu cần.

```ruby
num = 5.99
puts num.to_int  # Output: 5
```

---

### 9. **`truncate`**
Trả về `self` được cắt bỏ (về phía 0) đến độ chính xác được chỉ định.

```ruby
num = -3.14
puts num.truncate  # Output: -3

num = 2.999
puts num.truncate(1)  # Output: 2.9 (cắt bỏ đến 1 chữ số thập phân)
```

---

### Other
---

### 10. **`clone`**
Trả về bản sao của `self`, nhưng không cho phép đóng băng (freeze) đối tượng.

```ruby
str = "Hello"
str_clone = str.clone
puts str_clone  # Output: Hello
```

---

### 11. **`dup` (hoặc `+@`)**
Trả về bản sao của `self`.

```ruby
str = "Hello"
str_dup = str.dup
puts str_dup  # Output: Hello
```

---

### 12. **`step`**
Gọi khối lệnh với một chuỗi số được chỉ định.

```ruby
1.step(10, 2) { |i| puts i }
# Output:
# 1
# 3
# 5
# 7
# 9
```

---

### 13. **`upto`**
Gọi khối lệnh với các giá trị từ `self` đến giá trị đích.

```ruby
1.upto(5) { |i| puts i }
# Output:
# 1
# 2
# 3
# 4
# 5
```

---

#### to_s
Returns the string representation of self.
```ruby
1.to_s
=> "1"

7.to_s(2)
=> "111"

7.to_s(3)
=> "21"
```