# Dò vết & Sửa lỗi nối chuỗi

## 1. Nguyên nhân lỗi

Các giá tiền là kiểu String nên:

```javascript
"55000" + "15000"
````

bị nối thành:

```text
5500015000
```

Do đó tổng tiền cũng bị sai.

## 2. Cách sửa

Dùng `Number()` để ép kiểu:

```javascript
const foodPrice = Number(rawFoodPrice);
const toppingPrice = Number(rawToppingPrice);
const deliveryFee = Number(rawDeliveryFee);
```

Kết quả:

```text
Tổng tiền món ăn: 70000 VND
Số tiền thanh toán thực tế: 80000 VND
```

## 3. Test Cases

| Test |     Kết quả sai | Kết quả đúng |
| ---- | --------------: | -----------: |
| TC01 |      5500015000 |        70000 |
| TC02 | 550001500020000 |        80000 |

## 4. Kiến thức

* String và Number
* Ép kiểu `Number()`
* Toán tử `+`, `-`
* Template Literals

