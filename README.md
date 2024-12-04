# ASSIGNMENT-WEEK-3
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying a discount.
    
    Parameters:
        price (float): The original price of the item.
        discount_percent (float): The discount percentage to apply.
        
    Returns:
        float: The final price after applying the discount, or the original price if no discount is applied.
    """
    if discount_percent >= 20:
        final_price = price - (price * discount_percent / 100)
        return final_price
    else:
        return price

# Prompt the user for input
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percentage = float(input("Enter the discount percentage: "))

    # Calculate the final price using the function
    final_price = calculate_discount(original_price, discount_percentage)

    # Display the result
    if discount_percentage >= 20:
        print(f"After applying a {discount_percentage}% discount, the final price is: ${final_price:.2f}")
    else:
        print(f"No discount applied. The original price remains: ${original_price:.2f}")

except ValueError:
    print("Please enter valid numbers for the price and discount percentage.")
