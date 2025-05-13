# PLP-Python-wk-3a
def calculate_discount(price, discount_percent):
    """Calculates the final price after applying discount if discount is 20% or more."""
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Prompting the user for input
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(original_price, discount_percent)

    if discount_percent >= 20:
        print(f"Discount applied. The final price is: {final_price:.2f}")
    else:
        print(f"No discount applied. The final price remains: {final_price:.2f}")
except ValueError:
    print("Please enter valid numeric values for price and discount.")
