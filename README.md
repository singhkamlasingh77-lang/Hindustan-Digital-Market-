<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hindustan Digital Market</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-gray-100 font-sans text-gray-800">

    <!-- Header / Navbar -->
    <header class="bg-blue-900 text-white shadow-md">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <h1 class="text-xl md:text-2xl font-bold tracking-wide text-orange-400">
                Hindustan <span class="text-white">Digital Market</span>
            </h1>
            <button onclick="toggleAuthModal()" class="bg-orange-500 hover:bg-orange-600 text-white px-4 py-2 rounded-lg font-medium transition">
                Login / Register
            </button>
        </div>
    </header>

    <!-- Auth Modal (Login / Register) -->
    <div id="authModal" class="fixed inset-0 bg-black bg-opacity-50 hidden flex items-center justify-center p-4 z-50">
        <div class="bg-white rounded-2xl shadow-xl w-full max-w-md p-6 relative">

            <!-- Close Button -->
            <button onclick="toggleAuthModal()" class="absolute top-4 right-4 text-gray-500 hover:text-gray-800 text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <!-- Modal Tabs -->
            <div class="flex border-b mb-6">
                <button id="loginTab" onclick="switchAuthTab('login')" class="w-1/2 pb-2 font-semibold text-blue-900 border-b-2 border-blue-900">Login</button>
                <button id="registerTab" onclick="switchAuthTab('register')" class="w-1/2 pb-2 font-semibold text-gray-400 border-b-2 border-transparent">Register</button>
            </div>

            <!-- Login Form -->
            <form id="loginForm" class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700">Email or Phone</label>
                    <input type="text" placeholder="Enter email or phone" class="w-full mt-1 p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900" required>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">Password</label>
                    <input type="password" placeholder=" @  @  @  @  @  "w-full mt-1 p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900"s:ring-blue-900" required>
                </div>
                <button type="submit" class="w-full bg-blue-900 text-white py-2 rounded-lg font-semibold hover:bg-blue-800 transition">Log In</button>
            </form>

            <!-- Register Form (Hidden by default) -->
            <form id="registerForm" class="space-y-4 hidden">
                <div>
                    <label class="block text-sm font-medium text-gray-700">Full Name</label>
                    <input type="text" placeholder="Enter full name" class="w-full mt-1 p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900" required>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">Email or Phone</label>
                    <input type="text" placeholder="Enter email or phone number" class="w-full mt-1 p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900" required>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">Password</label>
                    <input type="password" placeholder=" @  @  @  @  @  "w-full mt-1 p-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900"s:ring-blue-900" required>
                </div>
                <button type="submit" class="w-full bg-orange-500 text-white py-2 rounded-lg font-semibold hover:bg-orange-600 transition">Create Account</button>
            </form>

            <!-- Social Login Divider -->
            <div class="relative my-6">
                <div class="absolute inset-0 flex items-center"><div class="w-full border-t border-gray-300"></div></div>
                <div class="relative flex justify-center text-sm"><span class="px-2 bg-white text-gray-500">Or continue with</span></div>
            </div>

            <!-- Social Login Buttons -->
            <div class="grid grid-cols-2 gap-3">
                <button class="flex items-center justify-center gap-2 border py-2 rounded-lg hover:bg-gray-50 transition">
                    <i class="fa-brands fa-google text-red-500"></i> Google
                </button>
                <button class="flex items-center justify-center gap-2 border py-2 rounded-lg hover:bg-gray-50 transition">
                    <i class="fa-brands fa-facebook text-blue-600"></i> Facebook
                </button>
            </div>

        </div>
    </div>
