# Boston-Data
It looks like you've created a simple HTML document that analyzes a paragraph and displays the three most frequently occurring words along with their counts. The code is well-structured and easy to follow. Here are a few suggestions:

1. **Heading Placement:** Consider adjusting the `h1` element's margin and text-shadow properties. You might want to center the heading, and you have a typo ("frist" should be "first").

   ```css
   h1 {
     text-shadow: 1px 2px grey;
     text-align: center;
   }
   ```

2. **JavaScript Logic:** The logic for counting and sorting words is well-implemented. However, you can use the `sort` method directly on the array returned by `Object.entries(counter)` for better readability.

   ```javascript
   var arr = Object.entries(counter).sort((a, b) => b[1] - a[1]);
   ```

   This sorts the array in descending order based on the count.

3. **Variable Naming:** Variable names like `paralower`, `anotherPara`, and `splitpara` might be improved for clarity. Consider using more descriptive names.

   ```javascript
   var lowercasedParagraph = paragraph.toLowerCase();
   var cleanedParagraph = lowercasedParagraph.replace(/[.,!\/;:"\n|\t]/g, ' ');
   var wordsArray = cleanedParagraph.split(" ").filter(word => word !== "");
   ```

4. **HTML Structure:** Consider adding some explanatory text or comments in the HTML to provide context for what the page is doing.

   ```html
   <!-- Displaying the three most frequently occurring words in a paragraph -->
   ```

With these changes, your code will be even more readable and maintainable. Overall, your code is well-organized and achieves the desired functionality. Great job!
