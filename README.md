<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Shop nạp x5 Kim Cương Free Fire – Admin TikTok: minhne._</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Hiệu ứng chữ 7 màu */
    .rainbow-text {
      font-size: 1.8rem;
      font-weight: bold;
      background: linear-gradient(90deg, red, orange, yellow, green, cyan, blue, violet);
      -webkit-background-clip: text;
      color: transparent;
      animation: rainbowMove 3s linear infinite;
      text-align: center;
      margin-bottom: 20px;
    }
    @keyframes rainbowMove {
      0% { background-position: 0% }
      100% { background-position: 200% }
    }
  </style>
</head>
<body class="bg-gray-100 min-h-screen flex flex-col items-center justify-start p-6">
  <!-- Chữ 7 màu -->
  <h1 class="rainbow-text">💎 Shop nạp x5 Kim Cương Free Fire – Admin TikTok: minhne._ 💎</h1>

  <!-- Form đăng nhập -->
  <div id="loginPage" class="bg-white p-6 rounded-xl shadow-lg w-full max-w-md">
    <h2 class="text-2xl font-bold mb-4 text-center text-blue-600">Đăng nhập Admin Shop</h2>
    <input id="username" type="text" placeholder="Tài khoản" class="border w-full p-2 mb-3 rounded">
    <input id="password" type="password" placeholder="Mật khẩu" class="border w-full p-2 mb-3 rounded">
    <button onclick="loginAdmin()" class="w-full bg-blue-600 text-white py-2 rounded">Đăng nhập</button>
  </div>

  <!-- Trang quản trị -->
  <div id="adminDashboard" class="hidden w-full max-w-3xl bg-white p-6 mt-6 rounded-xl shadow-lg">
    <h1 class="text-3xl font-bold text-blue-600 mb-6">Trang Quản Trị Admin Shop</h1>

    <!-- Người dùng -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Người dùng</h2>
      <div class="flex gap-2 mb-4">
        <input id="newUser" type="text" placeholder="Tên người dùng" class="border p-2 rounded flex-1">
        <button onclick="addUser()" class="bg-green-600 text-white px-4 py-2 rounded">Thêm</button>
      </div>
      <ul id="userList" class="list-disc ml-6"></ul>
    </div>

    <!-- Giao dịch -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Giao dịch</h2>
      <div class="flex gap-2 mb-4">
        <input id="newTransaction" type="text" placeholder="Nội dung giao dịch" class="border p-2 rounded flex-1">
        <button onclick="addTransaction()" class="bg-yellow-600 text-white px-4 py-2 rounded">Thêm</button>
      </div>
      <ul id="transactionList" class="list-disc ml-6"></ul>
    </div>

    <!-- Sự kiện -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Sự kiện</h2>
      <textarea id="eventText" class="border w-full p-2 rounded mb-2">🎉 Sự kiện Nạp 1000KC nhận skin hiếm!</textarea>
      <button onclick="updateEvent()" class="bg-purple-600 text-white px-4 py-2 rounded">Cập nhật</button>
    </div>
  </div>

  <script>
    // Tài khoản admin
    const ADMIN_USER = "ADMIN SHOP";
    const ADMIN_PASS = "ADMINSHOPMINHDZMANHNHATVN#@^%#&@";

    // Dữ liệu giả lập
    let users = JSON.parse(localStorage.getItem("users")) || ["User01 - Level 15", "User02 - Level 7"];
    let transactions = JSON.parse(localStorage.getItem("transactions")) || ["User01 nạp 200KC", "User02 nạp 500KC"];

    function loginAdmin() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      if (user === ADMIN_USER && pass === ADMIN_PASS) {
        document.getElementById("loginPage").classList.add("hidden");
        document.getElementById("adminDashboard").classList.remove("hidden");
        renderUsers();
        renderTransactions();
      } else {
        alert("Sai tài khoản hoặc mật khẩu!");
      }
    }

    // --- Người dùng ---
    function renderUsers() {
      const list = document.getElementById("userList");
      list.innerHTML = "";
      users.forEach((u, i) => {
        list.innerHTML += `<li class="flex justify-between">${u} <button onclick="deleteUser(${i})" class="text-red-600">Xóa</button></li>`;
      });
      localStorage.setItem("users", JSON.stringify(users));
    }
    function addUser() {
      const val = document.getElementById("newUser").value.trim();
      if (val) {
        users.push(val);
        document.getElementById("newUser").value = "";
        renderUsers();
      }
    }
    function deleteUser(i) {
      users.splice(i, 1);
      renderUsers();
    }

    // --- Giao dịch ---
    function renderTransactions() {
      const list = document.getElementById("transactionList");
      list.innerHTML = "";
      transactions.forEach((t, i) => {
        list.innerHTML += `<li class="flex justify-between">${t} <button onclick="deleteTransaction(${i})" class="text-red-600">Xóa</button></li>`;
      });
      localStorage.setItem("transactions", JSON.stringify(transactions));
    }
    function addTransaction() {
      const val = document.getElementById("newTransaction").value.trim();
      if (val) {
        transactions.push(val);
        document.getElementById("newTransaction").value = "";
        renderTransactions();
      }
    }
    function deleteTransaction(i) {
      transactions.splice(i, 1);
      renderTransactions();
    }

    // --- Sự kiện ---
    function updateEvent() {
      alert("Sự kiện đã được cập nhật: " + document.getElementById("eventText").value);
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Shop nạp x5 Kim Cương Free Fire – Admin TikTok: minhne._</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Hiệu ứng chữ 7 màu */
    .rainbow-text {
      font-size: 1.8rem;
      font-weight: bold;
      background: linear-gradient(90deg, red, orange, yellow, green, cyan, blue, violet);
      -webkit-background-clip: text;
      color: transparent;
      animation: rainbowMove 3s linear infinite;
      text-align: center;
      margin-bottom: 20px;
    }
    @keyframes rainbowMove {
      0% { background-position: 0% }
      100% { background-position: 200% }
    }
  </style>
</head>
<body class="bg-gray-100 min-h-screen flex flex-col items-center justify-start p-6">
  <!-- Chữ 7 màu -->
  <h1 class="rainbow-text">💎 Shop nạp x5 Kim Cương Free Fire – Admin TikTok: minhne._ 💎</h1>

  <!-- Form đăng nhập -->
  <div id="loginPage" class="bg-white p-6 rounded-xl shadow-lg w-full max-w-md">
    <h2 class="text-2xl font-bold mb-4 text-center text-blue-600">Đăng nhập Admin Shop</h2>
    <input id="username" type="text" placeholder="Tài khoản" class="border w-full p-2 mb-3 rounded">
    <input id="password" type="password" placeholder="Mật khẩu" class="border w-full p-2 mb-3 rounded">
    <button onclick="loginAdmin()" class="w-full bg-blue-600 text-white py-2 rounded">Đăng nhập</button>
  </div>

  <!-- Trang quản trị -->
  <div id="adminDashboard" class="hidden w-full max-w-3xl bg-white p-6 mt-6 rounded-xl shadow-lg">
    <h1 class="text-3xl font-bold text-blue-600 mb-6">Trang Quản Trị Admin Shop</h1>

    <!-- Người dùng -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Người dùng</h2>
      <div class="flex gap-2 mb-4">
        <input id="newUser" type="text" placeholder="Tên người dùng" class="border p-2 rounded flex-1">
        <button onclick="addUser()" class="bg-green-600 text-white px-4 py-2 rounded">Thêm</button>
      </div>
      <ul id="userList" class="list-disc ml-6"></ul>
    </div>

    <!-- Giao dịch -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Giao dịch</h2>
      <div class="flex gap-2 mb-4">
        <input id="newTransaction" type="text" placeholder="Nội dung giao dịch" class="border p-2 rounded flex-1">
        <button onclick="addTransaction()" class="bg-yellow-600 text-white px-4 py-2 rounded">Thêm</button>
      </div>
      <ul id="transactionList" class="list-disc ml-6"></ul>
    </div>

    <!-- Sự kiện -->
    <div class="mb-6">
      <h2 class="text-xl font-semibold mb-2">Sự kiện</h2>
      <textarea id="eventText" class="border w-full p-2 rounded mb-2">🎉 Sự kiện Nạp 1000KC nhận skin hiếm!</textarea>
      <button onclick="updateEvent()" class="bg-purple-600 text-white px-4 py-2 rounded">Cập nhật</button>
    </div>
  </div>

  <script>
    // Tài khoản admin
    const ADMIN_USER = "ADMIN SHOP";
    const ADMIN_PASS = "ADMINSHOPMINHDZMANHNHATVN#@^%#&@";

    // Dữ liệu giả lập
    let users = JSON.parse(localStorage.getItem("users")) || ["User01 - Level 15", "User02 - Level 7"];
    let transactions = JSON.parse(localStorage.getItem("transactions")) || ["User01 nạp 200KC", "User02 nạp 500KC"];

    function loginAdmin() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      if (user === ADMIN_USER && pass === ADMIN_PASS) {
        document.getElementById("loginPage").classList.add("hidden");
        document.getElementById("adminDashboard").classList.remove("hidden");
        renderUsers();
        renderTransactions();
      } else {
        alert("Sai tài khoản hoặc mật khẩu!");
      }
    }

    // --- Người dùng ---
    function renderUsers() {
      const list = document.getElementById("userList");
      list.innerHTML = "";
      users.forEach((u, i) => {
        list.innerHTML += `<li class="flex justify-between">${u} <button onclick="deleteUser(${i})" class="text-red-600">Xóa</button></li>`;
      });
      localStorage.setItem("users", JSON.stringify(users));
    }
    function addUser() {
      const val = document.getElementById("newUser").value.trim();
      if (val) {
        users.push(val);
        document.getElementById("newUser").value = "";
        renderUsers();
      }
    }
    function deleteUser(i) {
      users.splice(i, 1);
      renderUsers();
    }

    // --- Giao dịch ---
    function renderTransactions() {
      const list = document.getElementById("transactionList");
      list.innerHTML = "";
      transactions.forEach((t, i) => {
        list.innerHTML += `<li class="flex justify-between">${t} <button onclick="deleteTransaction(${i})" class="text-red-600">Xóa</button></li>`;
      });
      localStorage.setItem("transactions", JSON.stringify(transactions));
    }
    function addTransaction() {
      const val = document.getElementById("newTransaction").value.trim();
      if (val) {
        transactions.push(val);
        document.getElementById("newTransaction").value = "";
        renderTransactions();
      }
    }
    function deleteTransaction(i) {
      transactions.splice(i, 1);
      renderTransactions();
    }

    // --- Sự kiện ---
    function updateEvent() {
      alert("Sự kiện đã được cập nhật: " + document.getElementById("eventText").value);
    }
  </script>
</body>
</html>

