# Product Card UI Design

Welcome to the **Product Card UI Design** project! 🎉  
This is a stylish and interactive product card showcasing the **Jordan Proto-Lyte** from the running collection. The card features a responsive design, allowing users to view product details and change the image and color of the product with a simple click! Perfect for any e-commerce or product display webpage.

## Features

- **Responsive Design** 📱💻
- **Interactive Color Selection** 🎨
- **Modern Styling** using **CSS** and **HTML**
- **Smooth Animations** for color changes and image transitions
- **No JavaScript dependencies** apart from jQuery for the color-changing functionality

---

## 🛠️ Technologies Used

- **HTML5** - for structuring the content.
- **CSS3** - for styling and layout design.
- **jQuery** - to handle interactive features like color change and image swap.

---

## 🎨 Preview

![Product Card UI](https://raw.githubusercontent.com/anuzbvbmaniac/Responsive-Product-Card---CSS-ONLY/master/assets/img/jordan_proto.png)
![Black them](https://github.com/user-attachments/assets/afb2a2cf-b638-4da6-a9fe-3f338e094a92)

---

## 🚀 Getting Started

### 1. Clone the Repository

Clone this repository to your local machine to get started:

```bash
git clone https://owais41111.github.io/Product-Card/
```

### 2. Open the `index.html` File

Once cloned, open the `index.html` file in your browser to see the design in action!

---

## 🔧 Customization

You can easily customize this product card to fit your needs by:

- **Changing the Image**: Replace the image URLs in the HTML code with your own product images.
- **Editing the Product Details**: Modify the text content inside `<h2>`, `<p>`, and `<h3>` tags to reflect your product’s name, description, and price.
- **Adjusting the Colors**: Change the color options in the CSS and HTML to match your branding or design preferences.

---

## 📱 Responsive Design

This product card design is fully **responsive** and adjusts its layout for different screen sizes, from desktop to mobile. You can test the responsiveness by resizing the browser window or viewing it on different devices.

---

## 💡 How It Works

- The **image** and **background color** of the product card change when you click on any of the available color options.
- The **active color** is highlighted with a border around the color dot. The background of the card, title, price, and button are dynamically updated based on the selected color.
- The **product image** also changes accordingly to match the selected color.

---

## 👨‍💻 Contributing

We welcome contributions! If you'd like to improve or enhance the project, feel free to fork the repository and submit a pull request. Here's how you can contribute:

1. **Fork the repository**
2. **Clone your fork** to your local machine
3. Make your changes in a new branch
4. **Commit your changes** and push them to your fork
5. **Create a pull request**

---

## 🌟 Acknowledgments

- Thanks to **Google Fonts** for the **Poppins** font.
- **jQuery** for providing easy-to-use JS functionality.

---

Happy coding! 🚀✨

---

### Example HTML and CSS Files

Here are the HTML and CSS files used for this project.

#### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Product Card</title>
    <link rel="stylesheet" href="./style.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
</head>
<body>

    <div class="container">
        <div class="imgBx">
            <img src="https://github.com/anuzbvbmaniac/Responsive-Product-Card---CSS-ONLY/blob/master/assets/img/jordan_proto.png?raw=true" alt="Nike Jordan Proto-Lyte Image">
        </div>
        <div class="details">
            <div class="content">
                <h2>Jordan Proto-Lyte <br><span>Running Collection</span></h2>
                <p>
                    Featuring soft foam cushioning and lightweight, woven fabric in the upper, the Jordan Proto-Lyte is made for all-day, bouncy comfort.
                </p>
                <p class="product-colors">Available Colors:
                    <span class="black active" data-color-primary="#000" data-color-sec="#212121" data-pic="https://github.com/anuzbvbmaniac/Responsive-Product-Card---CSS-ONLY/blob/master/assets/img/jordan_proto.png?raw=true"></span>
                    <span class="red" data-color-primary="#7E021C" data-color-sec="#bd072d" data-pic="https://github.com/anuzbvbmaniac/Responsive-Product-Card---CSS-ONLY/blob/master/assets/img/jordan_proto_red_black.png?raw=true"></span>
                    <span class="orange" data-color-primary="#CE5B39" data-color-sec="#F18557" data-pic="https://github.com/anuzbvbmaniac/Responsive-Product-Card---CSS-ONLY/blob/master/assets/img/jordan_proto_orange_black.png?raw=true"></span>
                </p>
                <h3>Rs. 12,800</h3>
                <button>Buy Now</button>
            </div>
        </div>
    </div>

    <script>
        $(".product-colors span").click(function () {
            $(".product-colors span").removeClass("active");
            $(this).addClass("active");
            $(".active").css("border-color", $(this).attr("data-color-sec"));
            $("body").css("background", $(this).attr("data-color-primary"));
            $(".content h2").css("color", $(this).attr("data-color-sec"));
            $(".content h3").css("color", $(this).attr("data-color-sec"));
            $(".container .imgBx").css("background", $(this).attr("data-color-sec"));
            $(".container .details button").css("background", $(this).attr("data-color-sec"));
            $(".imgBx img").attr('src', $(this).attr("data-pic"));
        });
    </script>
</body>
</html>
```

#### `style.css`

```css
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,800&display=swap');
body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    font-family: 'Poppins', sans-serif;
    background: #000;
}

.container {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 900px;
    height: 600px;
    background: #fff;
    margin: 20px;
}

/* Add other CSS rules here */

.product-colors span {
    width: 26px;
    height: 26px;
    top: 7px;
    margin-right: 12px;
    left: 10px;
    border-radius: 50%;
    position: relative;
    cursor: pointer;
    display: inline-block;
}
```
