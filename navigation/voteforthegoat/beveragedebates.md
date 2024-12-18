---
layout: post
title: Beverage Debates
menu: nav/vote_for_the_goat.html
permalink: /voteforthegoat/beveragedebates/
author: Thomas, Collin
---

Our group has chosen to focus on discussions about which drinks should be added to our school cafeteria menu. For instance, we might consider whether options like flavored water or fruit juices should be introduced alongside traditional choices like chocolate milk. By exploring these topics, we aim to engage students in conversations that reflect their preferences and encourage them to share their opinions on beverage options.


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beverage Voting</title>
    <style>
        /* Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        /* Body Styling */
        body {
            background: linear-gradient(135deg, #1d2671, #c33764);
            background-attachment: fixed; /* Makes background fixed */
            color: #ffffff;
            font-family: Arial, sans-serif;
            min-height: 100vh; /* Ensures it covers the viewport height */
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        /* Container Styling */
        .voting-container {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 12px;
            padding: 30px;
            width: 100%;
            max-width: 800px; /* Increased to accommodate side-by-side layout */
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
            margin: auto;
        }
        .voting-container:hover {
            transform: scale(1.05);
        }
        /* Header Styling */
        .voting-container h2 {
            color: #00c6ff;
            font-size: 24px;
            margin-bottom: 20px;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        /* Option Buttons Styling */
        .option-button {
            background: linear-gradient(135deg, #ff8a00, #e52e71);
            color: #ffffff;
            padding: 12px 20px;
            width: 200px;
            margin: 8px 0;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 16px;
            transition: background 0.3s ease, transform 0.2s ease;
            outline: none;
            display: block;
        }
        .option-button:hover {
            background: linear-gradient(135deg, #e52e71, #ff8a00);
            transform: scale(1.1);
            box-shadow: 0 4px 8px rgba(255, 138, 0, 0.3);
        }
        .option-button:active {
            transform: scale(0.95);
        }
        /* Selected Option Display */
        .selected-option {
            margin-top: 15px;
            font-size: 18px;
            font-weight: bold;
            color: #00e6ff;
            text-shadow: 0 1px 4px rgba(0, 0, 0, 0.2);
        }
        /* Submit Button Styling */
        .submit-button {
            background: linear-gradient(135deg, #00c6ff, #0072ff);
            color: #ffffff;
            padding: 12px 30px;
            margin-top: 20px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
            transition: background 0.3s ease, transform 0.2s ease;
            outline: none;
        }
        .submit-button:hover {
            background: linear-gradient(135deg, #0072ff, #00c6ff);
            transform: scale(1.1);
            box-shadow: 0 4px 8px rgba(0, 198, 255, 0.3);
        }
        .submit-button:active {
            transform: scale(0.95);
        }
        /* Reasoning Input Box */
        .reasoning-container {
            display: none;
            margin-top: 20px;
            text-align: center;
        }
        .reasoning-container textarea {
            width: 100%;
            max-width: 350px;
            height: 100px;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #00c6ff;
            background: rgba(255, 255, 255, 0.2);
            color: #ffffff;
            font-size: 16px;
            resize: none;
            outline: none;
        }
        .reasoning-submit {
            margin-top: 10px;
            background: linear-gradient(135deg, #00c6ff, #0072ff);
            color: #ffffff;
            padding: 10px 20px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 16px;
            transition: background 0.3s ease, transform 0.2s ease;
            outline: none;
        }
        .reasoning-submit:hover {
            background: linear-gradient(135deg, #0072ff, #00c6ff);
            transform: scale(1.1);
            box-shadow: 0 4px 8px rgba(0, 198, 255, 0.3);
        }
        .reasoning-submit:active {
            transform: scale(0.95);
        }
        /* Add some basic styling for the clickable image */
        .clickable-image {
            cursor: pointer;
            max-width: 100%;
            height: auto;
            transition: opacity 0.3s ease;
        }
        .clickable-image:hover {
            opacity: 0.8;
        }
        /* Add these new styles */
        .beverage-details {
            display: none;
            padding: 15px;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 8px;
            text-align: left;
            position: sticky;
            top: 20px;
        }

        .beverage-details img {
            max-width: 200px;
            border-radius: 8px;
            margin: 10px 0;
        }

        .beverage-details p {
            font-size: 14px;
            line-height: 1.4;
            color: #ffffff;
        }

        /* Add new styles for the layout */
        .voting-layout {
            display: flex;
            gap: 20px;
            justify-content: space-between;
        }

        .options-container {
            flex: 0 0 40%;
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
        }

        .details-container {
            flex: 0 0 55%;
            position: relative;
        }

        nav a:hover, .DNHS-title:hover {
            background: rgba(0, 0, 0, 0.7);
            color: #00e6ff;
            transform: scale(1.05);
        }

        .nav-container {
            border-bottom: 2px solid #00c6ff;
            background: transparent;
        }

        .header-container {
            background: transparent;
            padding: 20px;
        }

        /* Style for the DNHS Flocker title */
        .header-title, 
        h1, 
        .DNHS-title {  /* Use whichever class/element your title uses */
            background: transparent;
            color: #ffffff;
            font-family: Arial, sans-serif;
            padding: 12px 20px;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .header-title:hover,
        h1:hover,
        .DNHS-title:hover {
            transform: scale(1.1);
            text-shadow: 0 4px 8px rgba(255, 138, 0, 0.3);
        }

        .modal {
            display: none; /* Hidden by default */
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
        }

        .modal-content {
            background-color: #333;
            margin: 15% auto;
            padding: 20px;
            width: 80%;
            max-width: 600px;
            border-radius: 10px;
            color: #fff;
            text-align: center;
        }

        #closeModal {
            background-color: #00c6ff;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }

        #closeModal:hover {
            background-color: #00e6ff;
        }
    </style>
</head>
<body>
    <div id="guidelinesModal" class="modal">
        <div class="modal-content">
            <h2>Community Rules/Guidelines</h2>
            <ul>
                <li>Be Respectful: Keep things light and friendly.</li>
                <li>Keep it Family-Friendly: Use clean language.</li>
                <li>Stay On-Topic: Focus on the debate question.</li>
                <li>Vote Honestly: Vote once per debate.</li>
                <li>One Account Only: Just one account per person.</li>
            </ul>
            <button id="closeModal">I have read and acknowledged the rules</button>
        </div>
    </div>

    <div class="voting-container">
        <h2>Choose Your Beverage that you would like to be added to Del Norte Cafeteria</h2>
        <div class="voting-layout">
            <div class="options-container">
                <button class="option-button" onclick="selectOption('Coke')">Coke</button>
                <button class="option-button" onclick="selectOption('Gatorade')">Gatorade</button>
                <button class="option-button" onclick="selectOption('Banana milk')">Banana milk</button>
                <button class="option-button" onclick="selectOption('Coconut water')">Coconut water</button>
                <div class="selected-option" id="selectedOption">Your Choice: None</div>
                <button class="submit-button" onclick="submitVote()">Submit Vote</button>
                <input type="text" id="suggestionInput" placeholder="Suggest a new beverage" style="margin-top: 20px; padding: 10px; border-radius: 8px; border: 1px solid #00c6ff; background: rgba(255, 255, 255, 0.2); color: #ffffff; font-size: 16px; outline: none;">
                <button class="submit-button" onclick="submitSuggestion()">Submit Suggestion</button>
            </div>
            
            <div class="details-container">
                <div id="coke-details" class="beverage-details">
                    <img src="https://images.unsplash.com/photo-1622483767028-3f66f32aef97?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8Y29rZXxlbnwwfHwwfHx8MA%3D%3D" alt="Coca Cola">
                    <p>Ingredients: Carbonated Water, High Fructose Corn Syrup, Caramel Color, Phosphoric Acid, Natural Flavors, Caffeine</p>
                </div>

                <div id="gatorade-details" class="beverage-details">
                    <img src="https://www.kroger.com/product/images/large/right/0005200012324" alt="Gatorade">
                    <p>Ingredients: Water, Sugar, Dextrose, Citric Acid, Natural and Artificial Flavor, Salt, Sodium Citrate, Monopotassium Phosphate, Modified Food Starch, Red 40</p>
                </div>

                <div id="banana-milk-details" class="beverage-details">
                    <img src="https://m.media-amazon.com/images/I/6177MtlTnkL.jpg" alt="Banana Milk">
                    <p>Ingredients: Milk, Banana Puree, Sugar, Natural Flavors, Vitamins A & D</p>
                </div>

                <div id="coconut-water-details" class="beverage-details">
                    <img src="https://pics.walgreens.com/prodimg/476175/450.jpg" alt="Coconut Water">
                    <p>Ingredients: 100% Natural Coconut Water, No Added Sugar or Preservatives</p>
                </div>
            </div>
        </div>
        <!-- Reasoning Input Container -->
        <div class="reasoning-container" id="reasoningContainer">
            <h3>Why did you choose this beverage?</h3>
            <textarea id="reasoningText" placeholder="Enter your reasoning here..."></textarea>
            <button class="reasoning-submit" onclick="submitReasoning()">Submit Reasoning</button>
        </div>
    </div>
    <script>
        let selectedBeverage = null;
        
        function hideAllDetails() {
            const details = document.querySelectorAll('.beverage-details');
            details.forEach(detail => detail.style.display = 'none');
        }

        function selectOption(beverage) {
            selectedBeverage = beverage;
            document.getElementById('selectedOption').textContent = 'Your Choice: ' + beverage;
            
            // Hide all details first
            hideAllDetails();
            
            // Show details for selected beverage
            const detailsId = beverage.toLowerCase().replace(' ', '-') + '-details';
            document.getElementById(detailsId).style.display = 'block';
        }

        function submitVote() {
            if (selectedBeverage) {
                alert('Thank you for voting for ' + selectedBeverage + '!');
                // Show the reasoning input section
                document.getElementById('reasoningContainer').style.display = 'block';
            } else {
                alert('Please select a beverage before submitting your vote.');
            }
        }
        function submitReasoning() {
            const reasoning = document.getElementById('reasoningText').value;
            if (reasoning.trim()) {
                alert('Thank you for sharing your reasoning: ' + reasoning);
                // Hide the reasoning input section after submission
                document.getElementById('reasoningContainer').style.display = 'none';
                document.getElementById('reasoningText').value = ''; // Clear the text area
            } else {
                alert('Please enter a reasoning before submitting.');
            }
        }

        function submitSuggestion() {
            const suggestion = document.getElementById('suggestionInput').value;
            if (suggestion.trim()) {
                alert('Thank you for your suggestion: ' + suggestion);
                document.getElementById('suggestionInput').value = ''; // Clear the input field
            } else {
                alert('Please enter a suggestion before submitting.');
            }
        }

        document.addEventListener("DOMContentLoaded", function() {
            const modal = document.getElementById("guidelinesModal");
            const closeModal = document.getElementById("closeModal");

            // Show the modal on page load
            modal.style.display = "block";

            // Close the modal when the button is clicked
            closeModal.onclick = function() {
                modal.style.display = "none";
            }
        });
    </script>
</body>
</html>


