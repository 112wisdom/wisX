# WisdomX Global News and Sport

This is a static website for WisdomX Global News and Sport. It provides the latest news on various topics including sports, celebrities, science and technology, war, economics, health, entertainment, and politics.

## How to Make the Site Live

To make the site live using GitHub Pages, follow these steps:

1. **Push Your Changes to GitHub:**

   ```sh
   git add .
   git commit -m "Initial commit with website structure and content"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub.
   - Click on the "Settings" tab.
   - In the left sidebar, click on "Pages".
   - Under "Source", select the branch you want to use for GitHub Pages (usually `main` or `master`).
   - Click "Save".

3. **Access Your Live Site:**
   Your website will be published at `https://<your-username>.github.io/<repository-name>/`.
   For example, if your GitHub username is `112wisdom` and the repository name is `WisdomX_Global_News_and_Sport`, your website will be accessible at `https://112wisdom.github.io/WisdomX_Global_News_and_Sport/`.

## Files

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WisdomX Global News and Sport</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>WisdomX Global News and Sport</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#categories">Categories</a></li>
                <li><a href="#latest-news">Latest News</a></li>
                <li><a href="#ads">Product Ads</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="support.html">Support Us</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>Welcome to WisdomX Global News and Sport</h2>
        <p>Stay updated with the latest news from the world of sports and beyond. Explore different categories and read the latest articles.</p>
        <div class="ad">
            <!-- Ad placeholder -->
            <p>Ad: Your ad here</p>
        </div>
    </section>

    <section id="categories">
        <h2>Categories</h2>
        <ul>
            <li><a href="#football">Football</a></li>
            <li><a href="#basketball">Basketball</a></li>
            <li><a href="#tennis">Tennis</a></li>
            <li><a href="#cricket">Cricket</a></li>
            <li><a href="#celebrities">Celebrities</a></li>
            <li><a href="#science-tech">Science & Technology</a></li>
            <li><a href="#war">War</a></li>
            <li><a href="#economics">Economics</a></li>
            <li><a href="#health">Health</a></li>
            <li><a href="#entertainment">Entertainment</a></li>
            <li><a href="#politics">Politics</a></li>
        </ul>
    </section>

    <section id="latest-news">
        <h2>Latest News</h2>
        <div id="latestNewsContent">
            <!-- Latest news will be dynamically loaded here -->
        </div>
    </section>

    <section id="celebrities">
        <h2>Celebrities</h2>
        <div id="celebritiesNewsContent">
            <!-- Celebrities news will be dynamically loaded here -->
        </div>
    </section>

    <section id="science-tech">
        <h2>Science & Technology</h2>
        <div id="scienceTechNewsContent">
            <!-- Science & Technology news will be dynamically loaded here -->
        </div>
    </section>

    <section id="war">
        <h2>War</h2>
        <div id="warNewsContent">
            <!-- War news will be dynamically loaded here -->
        </div>
    </section>

    <section id="economics">
        <h2>Economics</h2>
        <div id="economicsNewsContent">
            <!-- Economics news will be dynamically loaded here -->
        </div>
    </section>

    <section id="health">
        <h2>Health</h2>
        <div id="healthNewsContent">
            <!-- Health news will be dynamically loaded here -->
        </div>
    </section>

    <section id="entertainment">
        <h2>Entertainment</h2>
        <div id="entertainmentNewsContent">
            <!-- Entertainment news will be dynamically loaded here -->
        </div>
    </section>

    <section id="politics">
        <h2>Politics</h2>
        <div id="politicsNewsContent">
            <!-- Politics news will be dynamically loaded here -->
        </div>
    </section>

    <section id="ads">
        <h2>Product Ads</h2>
        <div class="product-ad">
            <h3>Product 1</h3>
            <p>Amazing product that will change your life! <a href="https://example.com/product1" target="_blank">Buy now</a></p>
        </div>
        <div class="product-ad">
            <h3>Product 2</h3>
            <p>Top-rated product for all your needs. <a href="https://example.com/product2" target="_blank">Check it out</a></p>
        </div>
        <div class="product-ad">
            <h3>Product 3</h3>
            <p>Get the best deals on this incredible product. <a href="https://example.com/product3" target="_blank">Shop now</a></p>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Support</h2>
        <p>For any inquiries or support, please contact us through the following channels:</p>
        <ul>
            <li>Telegram: <a href="https://t.me/shanti12c" target="_blank">t.me/shanti12c</a></li>
            <li>WhatsApp: <a href="https://wa.me/2348026029402" target="_blank">+2348026029402</a></li>
            <li>Email: <a href="mailto:chiagoziewisdom763@gmail.com">chiagoziewisdom763@gmail.com</a></li>
        </ul>
    </section>

    <footer>
        <p>&copy; 2025 WisdomX Global News and Sport. All rights reserved.</p>
    </footer>

    <script>
        const apiKey = 'YOUR_NEWS_API_KEY';
        const sportsNewsUrl = `https://newsapi.org/v2/top-headlines?category=sports&apiKey=${apiKey}`;
        const celebritiesNewsUrl = `https://newsapi.org/v2/top-headlines?category=entertainment&apiKey=${apiKey}`;
        const scienceTechNewsUrl = `https://newsapi.org/v2/top-headlines?category=science&apiKey=${apiKey}`;
        const warNewsUrl = `https://newsapi.org/v2/everything?q=war&apiKey=${apiKey}`;
        const economicsNewsUrl = `https://newsapi.org/v2/top-headlines?category=business&apiKey=${apiKey}`;
        const healthNewsUrl = `https://newsapi.org/v2/top-headlines?category=health&apiKey=${apiKey}`;
        const entertainmentNewsUrl = `https://newsapi.org/v2/top-headlines?category=entertainment&apiKey=${apiKey}`;
        const politicsNewsUrl = `https://newsapi.org/v2/top-headlines?category=politics&apiKey=${apiKey}`;

        async function fetchNews(url) {
            const response = await fetch(url);
            const data = await response.json();
            return data.articles;
        }

        function renderNews(articles, elementId) {
            const newsContent = document.getElementById(elementId);
            newsContent.innerHTML = '';
            articles.forEach(article => {
                const articleElement = document.createElement('article');
                articleElement.innerHTML = `
                    <h4><a href="${article.url}" target="_blank">${article.title}</a></h4>
                    <p>${article.description}</p>
                `;
                newsContent.appendChild(articleElement);
            });
        }

        async function updateNews() {
            const sportsArticles = await fetchNews(sportsNewsUrl);
            renderNews(sportsArticles, 'latestNewsContent');

            const celebritiesArticles = await fetchNews(celebritiesNewsUrl);
            renderNews(celebritiesArticles, 'celebritiesNewsContent');

            const scienceTechArticles = await fetchNews(scienceTechNewsUrl);
            renderNews(scienceTechArticles, 'scienceTechNewsContent');

            const warArticles = await fetchNews(warNewsUrl);
            renderNews(warArticles, 'warNewsContent');

            const economicsArticles = await fetchNews(economicsNewsUrl);
            renderNews(economicsArticles, 'economicsNewsContent');

            const healthArticles = await fetchNews(healthNewsUrl);
            renderNews(healthArticles, 'healthNewsContent');

            const entertainmentArticles = await fetchNews(entertainmentNewsUrl);
            renderNews(entertainmentArticles, 'entertainmentNewsContent');

            const politicsArticles = await fetchNews(politicsNewsUrl);
            renderNews(politicsArticles, 'politicsNewsContent');
        }

        updateNews();
        setInterval(updateNews, 86400000); // Update news every day (86400000 milliseconds = 24 hours)
    </script>
</body>
</html>
```

### `support.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Support Us - WisdomX Global News and Sport</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Support Us</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="#bitcoin">Bitcoin</a></li>
                <li><a href="#usdt">USDT (TRC20)</a></li>
                <li><a href="#ethereum">Ethereum</a></li>
                <li><a href="#bank-card">Bank Card</a></li>
                <li><a href="#bank-account">Bank Account</a></li>
                <li><a href="#palmpay">PalmPay</a></li>
                <li><a href="#moniepoint">MoniePoint</a></li>
                <li><a href="#opay">OPay</a></li>
            </ul>
        </nav>
    </header>

    <section id="bitcoin">
        <h2>Support Us with Bitcoin</h2>
        <p>Wallet Address: <strong>bc1q0fra5fcl58wge2rna8v9k62uu7u7q5zpcu906</strong></p>
    </section>

    <section id="usdt">
        <h2>Support Us with USDT (TRC20)</h2>
        <p>Wallet Address: <strong>tgrmzkdhvfsfp4fkDjumfcsEhvd6xas99e</strong></p>
    </section>

    <section id="ethereum">
        <h2>Support Us with Ethereum</h2>
        <p>Wallet Address: <strong>0xff87affcao6e9c56b7a2446a8bf3d02d8b</strong></p>
    </section>

    <section id="bank-card">
        <h2>Support Us with Bank Card</h2>
        <p>Please use your bank card to make a donation.</p>
        <!-- Bank card payment integration goes here -->
    </section>

    <section id="bank-account">
        <h2>Support Us with Bank Account</h2>
        <p>Account Number: <strong>8026029402</strong></p>
        <p>Account Name: <strong>Udochukwu Wisdom</strong></p>
    </section>

    <section id="palmpay">
        <h2>Support Us with PalmPay</h2>
        <p>Account Number: <strong>8026029402</strong></p>
        <p>Account Name: <strong>Udochukwu Wisdom</strong></p>
    </section>

    <section id="moniepoint">
        <h2>Support Us with MoniePoint</h2>
        <p>Account Number: <strong>8026029402</strong></p>
        <p>Account Name: <strong>Udochukwu Wisdom</strong></p>
    </section>

    <section id="opay">
        <h2>Support Us with OPay</h2>
        <p>Account Number: <strong>8026029402</strong></p>
        <p>Account Name: <strong>Udochukwu Wisdom</strong></p>
    </section>

    <footer>
        <p>&copy; 2025 WisdomX Global News and Sport. All rights reserved.</p>
    </footer>
</body>
</html>
```

### `styles.css`

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 1rem;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

section {
    padding: 2rem;
    background-color: #fff;
    margin: 1rem;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

section h2 {
    margin-top: 0;
}

footer {
    text-align: center;
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}

.ad {
    background-color: #eee;
    padding: 1rem;
    margin: 1rem 0;
    text-align: center;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.product-ad {
    background-color: #f9f9f9;
    padding: 1rem;
    margin: 1rem 0;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.product-ad h3 {
    margin-top: 0;
}

article h4 {
    margin: 0 0 0.5rem 0;
}

article p {
    margin: 0 0 1rem 0;
}
```
