# TestCal
Testing a calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Real Estate Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }

        h1 {
            margin: 0;
            font-size: 24px;
        }

        .property {
            background-color: #fff;
            border: 1px solid #ddd;
            margin: 20px;
            padding: 20px;
        }

        .property img {
            max-width: 100%;
            height: auto;
        }

        .property h2 {
            font-size: 18px;
            margin: 10px 0;
        }

        .property p {
            font-size: 14px;
            margin: 5px 0;
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Real Estate Website</h1>
    </header>

    <div class="property">
        <img src="property1.jpg" alt="Property 1">
        <h2>Beautiful Home for Sale</h2>
        <p>Location: 123 Main Street</p>
        <p>Price: $500,000</p>
        <p>Bedrooms: 4</p>
        <p>Bathrooms: 3</p>
        <button onclick="showDetails('property1')">Show Details</button>
    </div>

    <div class="property">
        <img src="property2.jpg" alt="Property 2">
        <h2>Luxury Apartment</h2>
        <p>Location: 456 Park Avenue</p>
        <p>Price: $800,000</p>
        <p>Bedrooms: 2</p>
        <p>Bathrooms: 2</p>
        <button onclick="showDetails('property2')">Show Details</button>
    </div>

    <div class="property">
        <img src="property3.jpg" alt="Property 3">
        <h2>Spacious Villa</h2>
        <p>Location: 789 Lakeview Drive</p>
        <p>Price: $1,200,000</p>
        <p>Bedrooms: 5</p>
        <p>Bathrooms: 4</p>
        <button onclick="showDetails('property3')">Show Details</button>
    </div>

    <div id="propertyDetails" style="display: none;">
        <!-- Property details will be displayed here using JavaScript -->
    </div>

    <footer>
        &copy; 2023 Real Estate Website
    </footer>

    <script>
        function showDetails(propertyId) {
            const propertyDetails = document.getElementById("propertyDetails");
            const details = getPropertyDetails(propertyId); // Implement this function to fetch property details

            if (details) {
                propertyDetails.innerHTML = details;
                propertyDetails.style.display = "block";
            }
        }

        function getPropertyDetails(propertyId) {
            // You can fetch property details from a database or another data source here
            // For simplicity, returning static details here
            if (propertyId === 'property1') {
                return `
                    <h3>Property 1 Details</h3>
                    <p>This is a beautiful home with a spacious living area, a backyard garden, and a two-car garage. It is located in a quiet neighborhood near schools and parks.</p>
                `;
            } else if (propertyId === 'property2') {
                return `
                    <h3>Property 2 Details</h3>
                    <p>This luxury apartment features high-end finishes, stunning city views, and access to a fitness center and swimming pool. It is located in the heart of the city.</p>
                `;
            } else if (propertyId === 'property3') {
                return `
                    <h3>Property 3 Details</h3>
                    <p>This spacious villa offers a large outdoor pool, a private garden, and a modern kitchen. It is situated in a peaceful lakeside community.</p>
                `;
            } else {
                return `<p>Property details not available.</p>`;
            }
        }
    </script>
</body>
</html>
