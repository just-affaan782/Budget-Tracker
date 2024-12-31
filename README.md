# Budget Tracker

## Description
The Budget Tracker is a simple web application that helps users manage their finances by tracking income and expenses. The app allows users to add transactions, categorize them as either income or expense, and view a summary of their financial data, including total income, total expense, and net balance.

## Features
- **Add Transactions**: Input a description, amount, and type (income or expense) for each transaction.
- **Transaction List**: View a list of all transactions categorized by income or expense.
- **Summary Section**: Displays total income, total expense, and net balance dynamically updated as transactions are added.
- **Responsive Design**: Optimized for both desktop and mobile devices.

## Technologies Used
- **HTML**: Structure and layout of the web application.
- **CSS**: Styling for a clean and user-friendly interface.
- **JavaScript**: Logic for handling transactions, updating the UI, and managing the summary calculations.

## How to Use
1. Open the application in a web browser.
2. Fill out the transaction form by entering:
   - A brief description of the transaction.
   - The amount of the transaction.
   - Select the type (income or expense).
3. Click the "Add Transaction" button.
4. The transaction will be added to the list, and the summary section will update automatically.
5. View the list of transactions and the updated summary to keep track of your budget.

## File Structure
- **HTML**: Contains the structure of the application, including forms, summary, and transaction list.
- **CSS (Inline)**: Provides styling for the app, ensuring a visually appealing design.
- **JavaScript (Inline)**: Implements the functionality for adding transactions, updating the summary, and rendering the transaction list.

## Code Example
```html
<!-- Summary Section -->
<div class="summary">
  <h2>Summary</h2>
  <p>Total Income: <span id="total-income">0</span></p>
  <p>Total Expense: <span id="total-expense">0</span></p>
  <p>Net Balance: <span id="net-balance">0</span></p>
</div>
```

```javascript
function updateSummary() {
  const income = transactions
    .filter((t) => t.type === 'income')
    .reduce((sum, t) => sum + t.amount, 0);

  const expense = transactions
    .filter((t) => t.type === 'expense')
    .reduce((sum, t) => sum + t.amount, 0);

  const netBalance = income - expense;

  totalIncomeEl.textContent = income;
  totalExpenseEl.textContent = expense;
  netBalanceEl.textContent = netBalance;
}
```

## Future Enhancements
- Add the ability to delete transactions.
- Implement data persistence using local storage or a database.
- Include charts to visualize spending trends.
- Add user authentication for personalized budgets.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Acknowledgements
- Inspired by common personal finance tracking needs.
- Created using basic web development tools to demonstrate simplicity and functionality.

