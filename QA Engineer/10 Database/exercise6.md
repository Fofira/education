# Запросы к базам данных
## 1. Customers
1. Выбор всех данных из `Customers` (клиентов) где `City` (город) указан `London` или `Paris`  
![1Customers](/QA%20Engineer/10%20Database/requests/1Customers.png)
2. Выбор `Country` (стран) из `Customers` (клиентов), отсортированных по `Country` (странам)  
![2Customers](/QA%20Engineer/10%20Database/requests/2Customers.png)
3. Выбор `ContactName` (контактного лица), `Address` (адреса) и `PostalCode` (почтового индекса) из `Customers` (клиентов), где `Country` (страна) указана `UK`, отсортированных по `ContactName` (контактному лицу) в порядке `ASC` (по возрастанию, от меньших значений к большим - в алфавитном порядке)  
![3Customers](/QA%20Engineer/10%20Database/requests/3Customers.png)

## 2. Categories
1. Выбор всех данных из `Categories` (категорий)  
![1Categories](/QA%20Engineer/10%20Database/requests/1Categories.png)
2. Выбор всех данных из `Categories` (категорий), отсортированных по `CategoryName` (названию категории) в порядке `DESC` (по убыванию, от больших значений к меньшим)  
![2Categories](/QA%20Engineer/10%20Database/requests/2Categories.png)
3. Выбор `CategoryName` (названия категории) и `Description` (описания) из `Categories` (категорий), где описание содержит `fish` (рыбу)  
![3Categories](/QA%20Engineer/10%20Database/requests/3Categories.png)

## 3. Employees
1. Выбор всех данных из `Employees` (сотрудников)  
![1Employees](/QA%20Engineer/10%20Database/requests/1Employees.png)
2. Выбор всех данных из `Employees` (сотрудников), где `LastName` (фамилия) указана `Peacock`  
![2Employees](/QA%20Engineer/10%20Database/requests/2Employees.png)
3. Выбор `LastName` (фамилии), `FirstName` (имени) и `BirthDate` (даты рождения) из `Employees` (сотрудников), где `BirthDate` (дата рождения) больше или равна `1958-09-19`, отсортированных по `LastName` (фамилии) в порядке `ASC` (по возрастанию, от меньших значений к большим - в алфавитном порядке)  
![3Employees](/QA%20Engineer/10%20Database/requests/3Employees.png)

## 4. OrderDetails
1. Выбор всех данных из `OrderDetails` (деталей заказа)  
![1OrderDetails](/QA%20Engineer/10%20Database/requests/1OrderDetails.png)
2. Выбор всех данных из `OrderDetails` (деталей заказа), отсортированных по `OrderDetailID` (id деталей заказа) в порядке `DESC` (по убыванию, от больших значений к меньшим)  
![2OrderDetails](/QA%20Engineer/10%20Database/requests/2OrderDetails.png)
3. Выбор всех данных из `OrderDetails` (деталей заказа), где `Quantity` (количество) указано `40` или `10`,  отсортированных по `OrderDetailID` (id деталей заказа) в порядке `DESC` (по убыванию, от больших значений к меньшим)  
![3OrderDetails](/QA%20Engineer/10%20Database/requests/3OrderDetails.png)

## 5. Orders
1. Выбор всех данных из `Orders` (заказов)  
![1Orders](/QA%20Engineer/10%20Database/requests/1Orders.png)
2. Выбор всех данных из `Orders` (заказов), где `CustomerID` (id клиента) указан `76`  
![2Orders](/QA%20Engineer/10%20Database/requests/2Orders.png)
3. Выбор `OrderID` (id заказа), `CustomerID` (id покупателя) и `OrderDate` (даты заказа) из `Orders` (заказов), где `CustomerID` (id покупателя) указан `87` и `OrderDate` (дата заказа) больше `1996-08-01`, отсортированных по `OrderID` в порядке `DESC` (по убыванию, от больших значений к меньшим)  
![3Orders](/QA%20Engineer/10%20Database/requests/3Orders.png)

## 6. Products
1. Выбор всех данных из `Products` (продуктов)  
![1Products](/QA%20Engineer/10%20Database/requests/1Products.png)
2. Выбор всех данных из `Products` (продуктов), отсортированных по `ProductName` (названию продукта) в порядке `ASC` (по возрастанию, от меньших значений к большим - в алфавитном порядке)  
![2Products](/QA%20Engineer/10%20Database/requests/2Products.png)
3. Выбор `ProductID` (id продукта), `ProductName` (названия продукта), `Unit` (единиц) и `Price` (цены) из `Products` (продуктов), где `CategoryID` (id категории) указан `2` и `Price` (цена) меньше `30`, отсортированных по `Price` (цене) в порядке `DESC` (по убыванию, от больших значений к меньшим)  
![3Products](/QA%20Engineer/10%20Database/requests/3Products.png)

## 7. Shippers
1. Выбор всех данных из `Shippers` (грузоотправителей/доставщиков)  
![1Shippers](/QA%20Engineer/10%20Database/requests/1Shippers.png)
2. Выбор всех данных из `Shippers` (грузоотправителей/доставщиков) где `ShipperID` (id грузоотправителя/доставщика) указан `1`  
![2Shippers](/QA%20Engineer/10%20Database/requests/2Shippers.png)
3. Выбор `ShipperName` (названия грузоотправителя/доставщика) и `Phone` (телефона) из `Shippers` (грузоотправителей/доставщиков), где `Phone` (телефон) содержит в окончании `31`, отсортированных по `ShipperName` (названию грузоотправителя/доставщика) в порядке `ASC` (по возрастанию, от меньших значений к большим - в алфавитном порядке)  
![3Shippers](/QA%20Engineer/10%20Database/requests/3Shippers.png)

## 8. Suppliers
1. Выбор всех данных из `Suppliers` (поставщиков)  
![1Suppliers](/QA%20Engineer/10%20Database/requests/1Suppliers.png)
2. Выбор всех данных из `Suppliers` (поставщиков), где `City` (город) указан `Londona` или `Tokyo`  
![2Suppliers](/QA%20Engineer/10%20Database/requests/2Suppliers.png)
3. Выбор всех данных из `Suppliers` (поставщиков), где `Country` (страна) указана `USA` или `Spain`, отсортированных по `City` (городу) в порядке `DESC` (по убыванию, от больших значений к меньшим - в обратном алфавитном порядке)  
![3Suppliers](/QA%20Engineer/10%20Database/requests/3Suppliers.png)
