# Father-s-Day-wish
A website for father's day using HTML, CSS and JS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Father's Day</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #34dbd3;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
            transition: all 0.3s ease;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 80px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            animation: fadeIn 1.5s ease-in-out;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin: 0 auto 30px;
            animation: fadeIn 2s ease-in-out;
        }

        /* Card Styles */
        .card {
            background: white;
            border-radius: 10px;
            padding: 30px;
            margin: 30px 0;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .card h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            font-size: 2rem;
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
        }

        /* Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 250px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 15px;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }

        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
        }

        /* Message Form */
        .message-form {
            margin: 50px 0;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
            color: var(--primary-color);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--secondary-color);
            outline: none;
        }

        button {
            background-color: var(--secondary-color);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        button:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }

        /* Personalized Message */
        .personal-message {
            background: var(--primary-color);
            color: white;
            padding: 40px;
            border-radius: 10px;
            margin: 50px 0;
            display: none;
            animation: fadeIn 1s ease-in-out;
        }

        .personal-message h2 {
            color: var(--light-color);
            margin-bottom: 20px;
            text-align: center;
        }

        .personal-message-content {
            font-size: 1.2rem;
            line-height: 1.8;
            text-align: center;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideIn {
            from { transform: translateY(50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        footer {
            text-align: center;
            padding: 30px;
            background-color: var(--dark-color);
            color: white;
            margin-top: 50px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1.2rem;
            }
            .gallery {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="hero">
        <h1>Happy Father's Day</h1>
        <p>To the greatest dad in the world - thank you for everything you have done till!</p>
        <button id="heartBtn">❤️ Send Love</button>
    </div>

    <div class="container">
        <!-- Photo Gallery -->
        <div class="card">
            <h2> Favorite Memories Of Your's</h2>
            <div class="gallery">
                <div class="gallery-item">
                    <img src="C:\Users\dell\Downloads\831436ae-cd17-44be-b643-c9dd00efc03d.jpg" alt="My Handsome Father" />
                    <div class="gallery-caption">
                        <h3>My Superhero</h3>
                        <p>An unbreakable bond holding all the love and feelings wrapped inside a camera roll with 
                            thousands of memories
                        </p>
                    </div>
                </div>
                <div class="gallery-item">
                    <img src="C:\Users\dell\Downloads\930cf528-9e6d-4e76-bfe7-c08ecd3cb8c3.jpg" alt="My Supehero,My Role Model and My Everthing" />
                    <div class="gallery-caption">
                        <h3>Special Gift </h3>
                        <p>What name shall give you when you are my everything!I am always greateful for the support 
                            and encouragement you provide to me at my weakest phase of my life. Thank you for every Love
                            ,care and unconditional support.
                        </p>
                    </div>
                </div>
                <div class="gallery-item">
                    <img src="C:\Users\dell\Downloads\96bc957f-e7e9-4454-aae2-2da52e362e4b.jpg" alt="A bond of Love " />
                    <div class="gallery-caption">
                        <h3>A special page for My Father</h3>
                        <p>This Father's Day , I tired to make this page for you.Not only in Father's Day but you are always special for me.
                            I know Sometimes I get sad  and angry with you but trust me ,I also love you so much.I would always
                            choose to be your daugther even if the world ends . These words are not just enough to describe
                            all feelings and love for you.
                        </p>
                    </div>
                </div>
                
                    </div>
                </div>
            </div>
        </div>

        <!-- Personalized Message Section -->
        <div class="card">
            <h2>Send Dad a Personal Message</h2>
            <div class="message-form">
                <div class="form-group">
                    <label for="sender">Your Name</label>
                    <input type="text" id="sender" placeholder="Enter your name">
                </div>
                <div class="form-group">
                    <label for="message">Your Message</label>
                    <textarea id="message" placeholder="Write your special Father's Day message here"></textarea>
   <h2>A Sweet Note For You</h2>

In quiet strength, you stand so tall,
A guiding hand through life's great hall.
With every laugh and every tear,
You’ve built a fortress, always near.


The stories shared by evening light,
The lessons learned, the endless fight—
You taught me courage, hope, and grace,
In every challenge, your embrace.


So on this day, I give my praise,
For all you are, in countless ways.
Thank you, dear Dad, for all you do,
With all my love, I'm proud of you

                </div>
                <button id="generateMessage">Create Message</button>
            </div>

            <div id="personalMessage" class="personal-message">
                <h2>Your Special Message</h2>
            
                <div id="personalMessageContent" class="personal-message-content"></div>
            </div>
        </div>

        <!-- Why We Love You -->
        <div class="card">
            <h2>Why You're the Best Dad</h2>
            <ul id="reasonsList">
                <!-- Will be populated by JavaScript -->
            </ul>
            <button id="addReasonBtn">Add Another Reason</button>
        </div>
    </div>

    <footer>
        <p>With love for Father's Day © 2025  From your daugther="Diya Shrestha"</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Heart button animation
            const heartBtn = document.getElementById('heartBtn');
            heartBtn.addEventListener('click', function() {
                this.innerHTML = '❤️❤️❤️ Love Sent ❤️❤️❤️';
                this.style.backgroundColor = '#e74c3c';
                
                // Create floating hearts animation
                for (let i = 0; i < 20; i++) {
                    setTimeout(() => {
                        createFloatingHeart();
                    }, i * 200);
                }
            });

            function createFloatingHeart() {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.style.position = 'absolute';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = '-100px';
                heart.style.fontSize = Math.random() * 30 + 20 + 'px';
                heart.style.animation = 'float ' + (Math.random() * 3 + 2) + 's ease-in forwards';
                document.body.appendChild(heart);

                // Remove heart after animation
                setTimeout(() => {
                    heart.remove();
                }, 5000);
            }

            // Add styles for floating hearts
            const style = document.createElement('style');
            style.textContent = `
                @keyframes float {
                    0% {
                        transform: translateY(0) rotate(0deg);
                        opacity: 1;
                    }
                    100% {
                        transform: translateY(-100vh) rotate(360deg);
                        opacity: 0;
                    }
                }
            `;
            document.head.appendChild(style);

            // Reasons why dad is great
            const reasons = [
                "You've always been there when I needed you",
                "You teach me valuable life lessons",
                "Your jokes might be cheesy, but they make me smile",
                "You work hard to provide for our family",
                "Your hugs make everything better",
                "You believe in me even when I don't believe in myself"
            ];

            const reasonsList = document.getElementById('reasonsList');
            const addReasonBtn = document.getElementById('addReasonBtn');

            // Populate initial reasons
            reasons.forEach(reason => {
                addReasonToList(reason);
            });

            // Add new reason
            addReasonBtn.addEventListener('click', function() {
                const newReason = prompt("Add another reason why your dad is awesome:");
                if (newReason) {
                    addReasonToList(newReason);
                }
            });

            function addReasonToList(reasonText) {
                const reasonItem = document.createElement('li');
                reasonItem.textContent = reasonText;
                reasonItem.style.listStyle = 'none';
                reasonItem.style.padding = '10px';
                reasonItem.style.marginBottom = '5px';
                reasonItem.style.backgroundColor = '#f8f9fa';
                reasonItem.style.borderRadius = '5px';
                reasonItem.style.animation = 'slideIn 0.5s ease-out';
                reasonsList.appendChild(reasonItem);
            }

            // Generate personalized message
            const generateMessageBtn = document.getElementById('generateMessage');
            const personalMessage = document.getElementById('personalMessage');
            const personalMessageContent = document.getElementById('personalMessageContent');

            generateMessageBtn.addEventListener('click', function() {
                const sender = document.getElementById('sender').value || 'Your Child';
                const message = document.getElementById('message').value || 'You are the best dad in the world!';
                
                const today = new Date();
                const dateStr = today.toLocaleDateString('en-US', {
                    weekday: 'long',
                    year: 'numeric',
                    month: 'long',
                    day: 'numeric'
                });

                const fullMessage = `
                    <p>Dear Dad,</p>
                    <p>${message}</p>
                    <p>I wanted to take this special day to thank you for all the love and support you've given me throughout my life. No matter what challenges come our way, I know I can always count on you.</p>
                    <p>Thank you for the sacrifices you've made, the lessons you've taught, and the unconditional love you've shown.</p>
                    <p>With all my love,</p>
                    <p>${sender}</p>
                    <p><em>${dateStr}</em></p>
                `;

                personalMessageContent.innerHTML = fullMessage;
                personalMessage.style.display = 'block';
                
                // Print button for the message
                const printBtn = document.createElement('button');
                printBtn.textContent = 'Print This Message';
                printBtn.style.marginTop = '20px';
                printBtn.style.backgroundColor = '#e74c3c';
                printBtn.onclick = function() {
                    window.print();
                };
                
                if (!document.getElementById('printBtn')) {
                    printBtn.id = 'printBtn';
                    personalMessage.appendChild(printBtn);
                }
            });

            // Animate elements when they come into view
            const animateOnScroll = function() {
                const elements = document.querySelectorAll('.card, .hero h1, .hero p');
                
                elements.forEach(element => {
                    const elementPosition = element.getBoundingClientRect().top;
                    const screenPosition = window.innerHeight / 1.2;
                    
                    if (elementPosition < screenPosition) {
                        element.style.animation = 'fadeIn 1s ease-out forwards';
                    }
                });
            };

            window.addEventListener('scroll', animateOnScroll);
            animateOnScroll(); // Trigger on load for visible elements
        });
    </script>
</body>
</html>

