<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Wonderful Friend</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        .hearts-container::after {
            content: '❤️';
            position: absolute;
            animation: hearts 5s linear infinite;
            opacity: 0;
        }
        @keyframes hearts {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
                left: 10%;
            }
            100% {
                transform: translateY(-500px) rotate(960deg);
                opacity: 0;
                left: 90%;
            }
        }
    </style>
</head>
<body class="bg-gradient-to-b from-blue-50 to-purple-50 min-h-screen font-sans p-4 overflow-x-hidden">
    <div class="hearts-container fixed inset-0 pointer-events-none"></div>
    <div class="max-w-3xl mx-auto my-8">
        <!-- Header with floating elements -->
        <header class="text-center relative mb-12">
            <div class="floating inline-block mb-4">
               <a href="https://ibb.co/HLPVmLY1"><img src="https://i.ibb.co/35F7t5WG/cropped-508792007-1394516991768314-4488954000330636229-n-modified.png" alt="cropped-508792007-1394516991768314-4488954000330636229-n-modified" border="0"></a><br /><a target='_blank' href='https://nl.imgbb.com/'>free forum maken</a><br />
            </div>
            <h1 class="text-4xl md:text-5xl font-bold text-indigo-800 mb-2">Get Well Soon, Nishika!</h1>
            <p class="text-xl text-purple-600">Every day is one step closer to recovery ❤️</p>
        </header>

        <!-- Main content area -->
        <main class="bg-white rounded-2xl shadow-xl p-6 md:p-8 mb-8">
            <div class="flex flex-col md:flex-row gap-6 mb-8">
                <div class="md:w-1/3">
                    <div class="bg-blue-100 p-4 rounded-xl h-full flex items-center justify-center">
                        <img src="https://placehold.co/300x300" alt="Peaceful illustration of a patient in bed with flowers and sunshine streaming through window" class="rounded-lg" />
                    </div>
                </div>
                <div class="md:w-2/3">
                    <h2 class="text-2xl font-bold text-indigo-700 mb-4">A Special Message For You</h2>
                    <div class="prose prose-lg text-gray-700">
                        <p>Dear Nishika,</p>
                        <p>Right now might be tough, but I want you to know how <span class="font-bold text-blue-600">strong</span> and <span class="font-bold text-blue-600">amazing</span> you are.</p>
                        <p>Every day, your body is healing, even when it doesn't feel like it. And every day, you're surrounded by people - including me - who love and admire you.</p>
                        <p>This hospital stay is just a small chapter in your incredible story. Soon you'll look back on this time as proof of your resilience.</p>
                    </div>
                </div>
            </div>

            <!-- Interactive elements -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
                <div class="bg-gradient-to-r from-blue-50 to-purple-50 p-6 rounded-xl border border-blue-200">
                    <h3 class="text-xl font-semibold text-indigo-700 mb-3">Your Healing Journey</h3>
                    <div class="w-full bg-gray-200 rounded-full h-4 mb-2">
                        <div id="progressBar" class="bg-gradient-to-r from-blue-400 to-purple-500 h-4 rounded-full" style="width: 25%"></div>
                    </div>
                    <p class="text-sm text-gray-600">Click to add to your progress!</p>
                    <button onclick="addProgress()" class="mt-3 px-4 py-2 bg-indigo-600 text-white rounded-lg hover:bg-indigo-700 transition">I Feel Better Today!</button>
                </div>
                <div class="bg-gradient-to-r from-purple-50 to-pink-50 p-6 rounded-xl border border-purple-200">
                    <h3 class="text-xl font-semibold text-indigo-700 mb-3">Virtual Hugs Received</h3>
                    <div id="hugCounter" class="text-4xl font-bold text-pink-600 mb-2">0</div>
                    <button onclick="sendHug()" class="px-4 py-2 bg-pink-500 text-white rounded-lg hover:bg-pink-600 transition">Send a Virtual Hug</button>
                </div>
            </div>

            <!-- Photo gallery placeholder -->
            <div class="mb-8">
                <h3 class="text-2xl font-bold text-center text-indigo-700 mb-6">Get Well Wishes</h3>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                    <div class="bg-blue-50 p-2 rounded-lg flex flex-col items-center">
                        <img src="https://placehold.co/200x200" alt="Close-up of sunflowers in a blue vase with warm sunlight" class="w-full h-32 object-cover rounded-md mb-2" />
                        <p class="text-sm text-center">Sunshine for brighter days</p>
                    </div>
                    <div class="bg-purple-50 p-2 rounded-lg flex flex-col items-center">
                        <img src="https://placehold.co/200x200" alt="Open book with healing symbols and a cup of tea" class="w-full h-32 object-cover rounded-md mb-2" />
                        <p class="text-sm text-center">Healing wisdom</p>
                    </div>
                    <div class="bg-pink-50 p-2 rounded-lg flex flex-col items-center">
                        <img src="https://placehold.co/200x200" alt="Colorful balloons floating upwards against blue sky" class="w-full h-32 object-cover rounded-md mb-2" />
                        <p class="text-sm text-center">Rising spirits</p>
                    </div>
                    <div class="bg-green-50 p-2 rounded-lg flex flex-col items-center">
                        <img src="https://placehold.co/200x200" alt="Serene forest path with sunlight filtering through trees" class="w-full h-32 object-cover rounded-md mb-2" />
                        <p class="text-sm text-center">Peaceful journey</p>
                    </div>
                </div>
            </div>

            <!-- Quotes section -->
            <div class="bg-gradient-to-r from-blue-600 to-purple-600 text-white p-6 rounded-xl mb-6">
                <h3 class="text-xl font-semibold mb-4">Today's Healing Thoughts</h3>
                <div id="quoteDisplay" class="text-lg italic mb-4">
                    "Healing is not an overnight process. It is a daily cleansing of pain, a daily healing of your life."
                </div>
                <button onclick="newQuote()" class="px-4 py-2 bg-white text-indigo-700 rounded-lg hover:bg-blue-100 transition">Another Thought</button>
            </div>
        </main>

        <!-- Personalized footer -->
        <footer class="text-center text-gray-600 mb-8">
            <p class="text-lg">Sending all my love, strength, and best wishes your way,</p>
            <p class="text-2xl font-bold text-purple-600 mt-2">K0CH1M4N4</p>
            <div class="mt-4">
                <button onclick="personalizeCard()" class="px-4 py-2 border-2 border-purple-500 text-purple-600 rounded-lg hover:bg-purple-50 transition">
                    Personalize This Card
                </button>
            </div>
        </footer>
    </div>

    <script>
        // Interactive elements functionality
        let progress = 25;
        let hugs = 0;
        const quotes = [
            "Healing is not an overnight process. It is a daily cleansing of pain, a daily healing of your life.",
            "Every day may not be good, but there's something good in every day.",
            "You're allowed to be both a masterpiece and a work in progress simultaneously.",
            "Healing comes in waves and maybe today the wave hits the rocks, but that's okay. You'll still come out on the other side.",
            "Your illness does not define you. Your strength and courage does.",
            "Every storm runs out of rain.",
            "This time will pass. You will get through it."
        ];

        function addProgress() {
            if (progress < 100) {
                progress += 5;
                if (progress > 100) progress = 100;
                document.getElementById('progressBar').style.width = `${progress}%`;
                showConfetti();
            } else {
                alert("You're fully recovered in our hearts! ❤️");
            }
        }

        function sendHug() {
            hugs++;
            document.getElementById('hugCounter').innerText = hugs;
            createHeart();
        }

        function newQuote() {
            const randomIndex = Math.floor(Math.random() * quotes.length);
            document.getElementById('quoteDisplay').innerText = quotes[randomIndex];
        }

        function showConfetti() {
            const colors = ['#FF5252', '#FF4081', '#E040FB', '#7C4DFF', '#536DFE'];
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'fixed h-2 w-2 rounded-full';
                    confetti.style.left = `${Math.random() * 100}%`;
                    confetti.style.top = '-10px';
                    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                    confetti.style.zIndex = '9999';
                    
                    const animation = confetti.animate([
                        { top: '-10px', opacity: 1 },
                        { top: `${Math.random() * 100 + 50}%, opacity: 0` }
                    ], {
                        duration: 2000,
                        easing: 'cubic-bezier(0.1, 0.8, 0.3, 1)',
                        fill: 'forwards'
                    });
                    
                    document.body.appendChild(confetti);
                    animation.onfinish = () => confetti.remove();
                }, i * 100);
            }
        }

        function createHeart() {
            const container = document.querySelector('.hearts-container');
            const heart = document.createElement('div');
            heart.className = 'hearts-container';
            heart.style.left = `${Math.random() * 100}%`;
            heart.style.animationDuration = `${3 + Math.random() * 4}s`;
            container.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }

        function personalizeCard() {
            const yourName = prompt("Enter your name:");
            if (yourName) {
                document.querySelector('footer p:last-child').textContent = yourName;
                document.title = `Get Well Nishika - From ${yourName}`;
            }
        }

        // Initialize with slight delay for animations
        setTimeout(() => {
            newQuote();
            document.querySelector('header').classList.add('animate-fadeIn');
        }, 300);
    </script>
</body>
</html>
