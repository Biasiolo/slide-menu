# Slide Menu

Welcome to Slide Menu, a simple jQuery-based project for creating a wide color button that opens a sliding menu.

## Getting Started

To use Slide Menu in your project, follow these steps:

1. Include jQuery in your HTML:

   ```html
   <script src="https://code.jquery.com/jquery-3.6.4.min.js"></script>
   ```

2. Add the CSS and JavaScript files:

   ```html
   <link rel="stylesheet" href="styles.css">
   <script src="script.js"></script>
   ```

3. Create a button with the class `fifth`:

   ```html
   <button class="fifth">Open Menu</button>
   ```

4. Add left and right modals with your desired content:

   ```html
   <div class="modal left">
       <!-- Left Modal Content -->
   </div>

   <div class="modal right">
       <!-- Right Modal Content -->
   </div>
   ```

5. Customize the styles in `styles.css` to fit your project's design.

6. Initialize the Slide Menu:

   ```javascript
   $(document).ready(function() {
       $(".fifth").click(function() {
           $(".modal.left").toggleClass("show-left");
           $(".modal.right").toggleClass("show-right");
       });

       $(document).mouseup(function(e) {
           var modal = $(".modal");

           if (!modal.is(e.target) && modal.has(e.target).length === 0) {
               modal.removeClass("show-left show-right");
           }
       });
   });
   ```

## Options

- `fifth`: The button class to trigger the sliding menu.
- `modal left` and `modal right`: Classes for left and right modals, respectively.

Feel free to explore and customize the project to suit your needs!

## License

This project is licensed under the [MIT License](LICENSE).
