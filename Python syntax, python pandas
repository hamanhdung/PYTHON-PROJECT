#                          Python syntax, python pandas

# Python syntax

Câu 1 (1đ): Số hoàn hảo (hay còn gọi là số hoàn chỉnh, số hoàn thiện hoặc số hoàn thành)
là một số nguyên dương mà tổng các ước nguyên dương thực sự của nó (các số nguyên dương
bị nó chia hết ngoại trừ nó) bằng chính nó.
In ra số lượng các số là số hoàn hảo trong khoảng giá trị từ 1 cho tới 10000.
VD: 6, 28, 496 là các số hoàn hảo


```python
def check_number(a):
    sum_number=1
    for i in range(2,int(a**(1/2))+1):
        if a%i==0:
            sum_number=sum_number+i+ (a//i)
    if sum_number==a:
        return True
        print(a)
    else:
        return False
amount=0
for i in range(1,10001):
    if (check_number(i)==True) and (i!=1):
        amount=amount+1
print(amount)
```

    4
    

Câu 2 (1đ): In ra 4 giá trị như sau: tổng giá trị của các số nguyên tố, tổng giá trị của các số chẵn,
tổng giá trị của các số là số chính phương, tổng giá trị của các số là bội số của 10 trong khoảng
giá trị từ 1 cho tới 10000.


```python
def check_prime_number(n):
    test=0
    if n==1: return False
    for i in range(2,int(n//2)+1):
        if n%i==0:
            test=1
            break
    if test==0:
        return True
    else:
        return False
sum_prime_number=0
sum_even_number=0
sum_square_number=0
sum_divisible_by_10=0
for i in range(1,10001):
    if check_prime_number(i)==True:
        sum_prime_number=sum_prime_number +i
    if i%2 ==0:
        sum_even_number=sum_even_number +i    
    if (int(i**(1/2))==i**(1/2)):
        sum_square_number=sum_square_number +i
    if i%10==0:
        sum_divisible_by_10=sum_divisible_by_10 +i
print(sum_prime_number)
print(sum_even_number)
print(sum_square_number)
print(sum_divisible_by_10)
```

    5736396
    25005000
    338350
    5005000
    

# Python pandas 
# Hiện thực Câu 1->3 của phần SQL bằng Pandas. Mỗi câu 0.75 điểm


```python
import pandas as pd
```


```python
Sales = pd.read_csv(r'C:\Users\Ha Manh Dung\Downloads\sales.csv')
```

Câu 1: Lấy thông tin về Mã đơn hàng, mã sản phẩm, mã khách hàng, số lượng sản phẩm của những dòng dữ liệu thỏa điều kiện Ship Mode là Standard Class


```python
Sales[Sales['Ship Mode'] == 'Standard Class'][['Order ID', 'Product ID','Customer ID', 'Quantity']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Order ID</th>
      <th>Product ID</th>
      <th>Customer ID</th>
      <th>Quantity</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>US-2015-108966</td>
      <td>FUR-TA-10000577</td>
      <td>SO-20335</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>US-2015-108966</td>
      <td>OFF-ST-10000760</td>
      <td>SO-20335</td>
      <td>2</td>
    </tr>
    <tr>
      <th>5</th>
      <td>CA-2014-115812</td>
      <td>FUR-FU-10001487</td>
      <td>BH-11710</td>
      <td>7</td>
    </tr>
    <tr>
      <th>6</th>
      <td>CA-2014-115812</td>
      <td>OFF-AR-10002833</td>
      <td>BH-11710</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>CA-2014-115812</td>
      <td>TEC-PH-10002275</td>
      <td>BH-11710</td>
      <td>6</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9987</th>
      <td>CA-2017-163629</td>
      <td>TEC-AC-10001539</td>
      <td>RA-19885</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9988</th>
      <td>CA-2017-163629</td>
      <td>TEC-PH-10004006</td>
      <td>RA-19885</td>
      <td>5</td>
    </tr>
    <tr>
      <th>9990</th>
      <td>CA-2017-121258</td>
      <td>FUR-FU-10000747</td>
      <td>DB-13060</td>
      <td>2</td>
    </tr>
    <tr>
      <th>9991</th>
      <td>CA-2017-121258</td>
      <td>TEC-PH-10003645</td>
      <td>DB-13060</td>
      <td>2</td>
    </tr>
    <tr>
      <th>9992</th>
      <td>CA-2017-121258</td>
      <td>OFF-PA-10004041</td>
      <td>DB-13060</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
<p>5968 rows × 4 columns</p>
</div>



Câu 2 : Lấy thông tin về mã đơn hàng thỏa mãn điều kiện có tồn tại một loại sản phẩm (Product ID) thuộc nhóm category là Office Supplies và có quantity > 3


```python
Sales[(Sales['Category'] == 'Office Supplies') & (Sales['Quantity'] > 3)][['Order ID']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Order ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>CA-2014-115812</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CA-2014-115812</td>
    </tr>
    <tr>
      <th>14</th>
      <td>US-2015-118983</td>
    </tr>
    <tr>
      <th>16</th>
      <td>CA-2014-105893</td>
    </tr>
    <tr>
      <th>20</th>
      <td>CA-2014-143336</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>9981</th>
      <td>CA-2017-163566</td>
    </tr>
    <tr>
      <th>9982</th>
      <td>US-2016-157728</td>
    </tr>
    <tr>
      <th>9984</th>
      <td>CA-2015-100251</td>
    </tr>
    <tr>
      <th>9985</th>
      <td>CA-2015-100251</td>
    </tr>
    <tr>
      <th>9992</th>
      <td>CA-2017-121258</td>
    </tr>
  </tbody>
</table>
<p>2614 rows × 1 columns</p>
</div>



Câu 3 : Thống kê số lượng mã đơn hàng, số lượng các loại sản phẩm (product ID), tổng doanh thu và tổng lợi nhuận theo từng Category, sắp xếp theo thứ tự giảm dần của doanh thu


```python
def f(x): 
    a = x['Order ID'].nunique()
    b = x['Product ID'].nunique()
    c = x['Profit'].sum()
    d = x.drop_duplicates('Category').Profit.sum()
    return pd.Series([a,b,c], index = [['Số lượng mã đơn hàng  ', '  Số lượng mã sản phẩm', '  Tổng lợi nhuận']])
```


```python
print(Sales.groupby(['Category']).apply(f))
```

                    Số lượng mã đơn hàng     Số lượng mã sản phẩm   Tổng lợi nhuận
    Category                                                                      
    Furniture                       1764.0                  375.0         18451.25
    Office Supplies                 3742.0                 1083.0        122490.88
    Technology                      1544.0                  404.0        145455.66
    
