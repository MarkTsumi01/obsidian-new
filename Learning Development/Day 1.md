## 1.ทำความเข้าใจ ERP 

- ERP คือซอฟต์แวร์ที่ถูกสร้างขึ้นมาเพื่อใช้งานในองค์กรณ์
- ERP จะรวมส่วนต่างๆในองค์กร เช่น การเงิน ทรัพยากรบุคคล อุปกรณ์ไอที หรือหลายๆส่วนเข้ามาด้วยกันเพื่อที่จะสามารถจัดการได้อย่างง่ายดาย
- ถูกพัฒนามาอย่างต่อเนื่องและยาวนาน
- ไม่จำกัดเฉพาะองค์กรขนาดใหญ่แต่องกรณ์ขนาดกลางและขนาดเล็กก็สามารถใช้งานได้
- มีหลายรูปแบบให้เลือกใช้ทั้งแบบ Cloud , On Premise 
- ช่วยเพิ่ม Productivity ให้องค์กรและช่วยลดความซับซ้อนและความไม่สะดวกในการบริหารจัดการทรัพยากร

## 2.SQL Basics

โจทย์ :
	หาลูกค้าที่อายุเกิน 25 ปี
	หาสินค้าที่ราคามากกว่า 500 บาท

คำตอบ 

หาลูกค้าที่อายุเกิน 25 ปี

```
	SELECT *
	FROM CUSTOMERS
	WHERE age > 25
```

หาสินค้าที่ราคามากกว่า 500 บาท

```
	SELECT *
	FROM PRODCUTS
	WHERE price > 500
```

## 3.Python Coding Exercise

โจทย์ :
	สร้าง Class Product และ Order
	เพิ่มสินค้าลงในคำสั่งซื้อ
	คำนวณราคารวม

```
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class Order:
    def __init__(self):
        self.items = []

    def add_items(self, product, quantity):
        self.items.append((product, quantity))

    def total_price(self):
        return sum(p.price * q for p, q in self.items)

    def show_items(self):
        for p, q in self.items:
            print(f"{p.name}: {q} x {p.price} = {p.price * q}")

p1 = Product("Keyboard", 500)
p2 = Product("Mouse", 200)

order = Order()
order.add_items(p1, 2)
order.add_items(p2, 3)
order.show_items()

print("Total", order.total_price())
```

## 3.ER Diagram

โจทย์:
		วาดระบบ Order Management
			Customer => Place => Order
			Order => Include => Product
![[Pasted image 20251209112448.png]]