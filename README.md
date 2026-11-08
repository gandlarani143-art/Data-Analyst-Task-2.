
import matplotlib.pyplot as plt

# DATA VISUALIZATION AND STORYTELLING
# Sample Superstore Sales Dataset

# Monthly Sales Data
months = [
    "Jan", "Feb", "Mar", "Apr",
    "May", "Jun", "Jul", "Aug",
    "Sep", "Oct", "Nov", "Dec"
]

monthly_sales = [
    12000, 15000, 18000, 14000,
    22000, 25000, 20000, 28000,
    30000, 26000, 35000, 40000
]

# Category Sales Data
categories = ["Furniture", "Technology", "Office Supplies"]
category_sales = [45000, 75000, 55000]

# Region Sales Data
regions = ["East", "West", "Central", "South"]
region_sales = [40000, 60000, 35000, 45000]

# Profit Data
profit = [8000, 18000, 12000]

# Create Dashboard
plt.figure(figsize=(12, 9))

# 1. Monthly Sales Chart
plt.subplot(2, 2, 1)
plt.plot(months, monthly_sales, marker="o")
plt.title("Monthly Sales Analysis")
plt.xlabel("Months")
plt.ylabel("Sales")
plt.xticks(rotation=45)
plt.grid(True)

# 2. Category Sales Chart
plt.subplot(2, 2, 2)
plt.bar(categories, category_sales)
plt.title("Category-wise Sales")
plt.xlabel("Categories")
plt.ylabel("Sales")
plt.xticks(rotation=20)

# 3. Region Sales Chart
plt.subplot(2, 2, 3)
plt.pie(
    region_sales,
    labels=regions,
    autopct="%1.1f%%",
    startangle=90
)
plt.title("Region-wise Sales")

# 4. Profit Analysis
plt.subplot(2, 2, 4)
plt.bar(categories, profit)
plt.title("Category-wise Profit")
plt.xlabel("Categories")
plt.ylabel("Profit")
plt.xticks(rotation=20)

plt.suptitle(
    "DATA VISUALIZATION AND STORYTELLING",
    fontsize=14
)

plt.tight_layout()

# Save Dashboard
plt.savefig("sales_dashboard.png")

# Display Dashboard
plt.show()

# Business Insights
print("\n===== BUSINESS INSIGHTS =====")

print("1. December has the highest monthly sales.")

print("2. Technology has the highest category sales.")

print("3. West region has the highest sales.")

print("4. Technology generates the highest profit.")

print("\nDashboard created successfully!")
print("File saved as sales_dashboard.png")
# Data-Analyst-Task-2.