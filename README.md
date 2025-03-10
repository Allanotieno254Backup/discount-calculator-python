# discount-calculator-python

# 🛒 Discount Calculator in Python

## 📌 Project Overview  
This Python project calculates the final price of an item after applying a discount. If the discount is **20% or higher**, it gets applied to the original price; otherwise, the original price remains unchanged. The program takes **user input** for the price and discount percentage, then displays the final price accordingly.

---

## 🚀 Features  
✅ Accepts user input for **price** and **discount percentage**  
✅ Applies the discount **only if it is 20% or more**  
✅ Returns the **original price** if the discount is below 20%  
✅ Provides **formatted output** with two decimal places  
✅ **Simple and easy-to-use** Python function  

---

## 🖥️ How It Works  
1. The user enters the **original price** of an item.  
2. The user enters the **discount percentage** they want to apply.  
3. If the discount is **20% or more**, the function applies the discount and prints the **final price**.  
4. If the discount is **less than 20%**, the function prints the **original price** without applying any discount.  

---

## 📝 Code Implementation  

```python
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount.

    Parameters:
    - price (float): Original price of the item
    - discount_percent (float): Discount percentage

    Returns:
    - float: Final price after applying the discount (if applicable)
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    return price  # Return original price if discount is less than 20%


# Get user input
price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Calculate the final price
final_price = calculate_discount(price, discount_percent)

# Print the result
if discount_percent >= 20:
    print(f"Discount applied! The final price is: ${final_price:.2f}")
else:
    print(f"No discount applied. The original price remains: ${price:.2f}")

## Example Outputs
Enter the original price of the item: 100
Enter the discount percentage: 25
Discount applied! The final price is: $75.00
