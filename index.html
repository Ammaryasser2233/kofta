<!doctype html>
<html lang="ar" dir="rtl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>كفتة على الفحم - نظام المطعم المتقدم</title>
    <!-- إضافة مكتبات خارجية -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-firestore-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-auth-compat.js"></script>
    <style>
      /* جميع الأنماط السابقة مع تحسينات */
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      :root {
        --primary-color: #ffd700;
        --secondary-color: #ff6b35;
        --dark-bg: #1a1a1a;
        --light-bg: #f5f5f5;
        --text-dark: #333;
        --text-light: #fff;
        --border-color: #ddd;
        --success-color: #4caf50;
        --error-color: #f44336;
        --warning-color: #ff9800;
        --info-color: #2196f3;
        --order-pending: #ffc107;
        --order-preparing: #2196f3;
        --order-ready: #4caf50;
        --order-delivered: #9e9e9e;
        --admin-color: #9c27b0;
        --cashier-color: #2196f3;
        --hold-color: #9c27b0;
      }

      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        background-color: var(--light-bg);
        color: var(--text-dark);
        line-height: 1.6;
        position: relative;
        transition: all 0.3s ease;
      }

      /* العلامة المائية */
      .watermark {
        position: fixed;
        bottom: 10px;
        left: 10px;
        font-size: 12px;
        color: rgba(0, 0, 0, 0.2);
        z-index: 9999;
        pointer-events: none;
        font-family: Arial, sans-serif;
        background: rgba(255, 255, 255, 0.3);
        padding: 5px 10px;
        border-radius: 3px;
        transform: rotate(-5deg);
      }

      .container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 20px;
      }

      /* ==================== تسجيل الدخول ==================== */
      .login-container {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background: linear-gradient(
          135deg,
          var(--secondary-color),
          var(--primary-color)
        );
        position: relative;
        overflow: hidden;
      }

      .login-container::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-image: url("https://images.unsplash.com/photo-1555939594-58d7cb561ad1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80");
        background-size: cover;
        background-position: center;
        opacity: 0.2;
        z-index: 0;
      }

      .login-box {
        background: white;
        padding: 40px;
        border-radius: 15px;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        width: 100%;
        max-width: 450px;
        text-align: center;
        position: relative;
        z-index: 1;
        animation: slideUp 0.5s ease-out;
      }

      @keyframes slideUp {
        from {
          opacity: 0;
          transform: translateY(30px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      .login-box .restaurant-logo {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        margin: 0 auto 20px;
        object-fit: cover;
        border: 4px solid var(--primary-color);
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
      }

      .login-box .restaurant-logo:hover {
        transform: scale(1.05);
      }

      .login-box h1 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 28px;
        text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
      }

      .login-box p {
        margin-bottom: 20px;
        color: #666;
        font-size: 14px;
      }

      .login-box .role-selector {
        display: flex;
        gap: 10px;
        margin-bottom: 30px;
        justify-content: center;
      }

      .login-box .role-btn {
        flex: 1;
        padding: 12px;
        border: 2px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-size: 14px;
        font-weight: bold;
        transition: all 0.3s;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
      }

      .login-box .role-btn i {
        font-size: 20px;
      }

      .login-box .role-btn.active {
        background: var(--primary-color);
        border-color: var(--secondary-color);
        color: var(--text-dark);
        transform: translateY(-3px);
        box-shadow: 0 5px 15px rgba(255, 107, 53, 0.2);
      }

      .form-group {
        margin-bottom: 20px;
        text-align: right;
      }

      .form-group label {
        display: block;
        margin-bottom: 8px;
        font-weight: bold;
        color: var(--text-dark);
      }

      .form-group input,
      .form-group select,
      .form-group textarea {
        width: 100%;
        padding: 12px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
        text-align: right;
        transition: all 0.3s;
      }

      .form-group input:focus,
      .form-group select:focus,
      .form-group textarea:focus {
        outline: none;
        border-color: var(--secondary-color);
        box-shadow: 0 0 5px rgba(255, 107, 53, 0.3);
      }

      .btn {
        padding: 12px 30px;
        border: none;
        border-radius: 8px;
        font-size: 16px;
        font-weight: bold;
        cursor: pointer;
        transition: all 0.3s;
        position: relative;
        overflow: hidden;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
      }

      .btn-primary {
        background: var(--secondary-color);
        color: white;
        width: 100%;
      }

      .btn-primary:hover {
        background: #ff5722;
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(255, 107, 53, 0.3);
      }

      .btn-secondary {
        background: var(--primary-color);
        color: var(--text-dark);
        margin-right: 10px;
      }

      .btn-secondary:hover {
        background: #ffc700;
      }

      .btn-danger {
        background: var(--error-color);
        color: white;
      }

      .btn-danger:hover {
        background: #e53935;
      }

      .btn-success {
        background: var(--success-color);
        color: white;
      }

      .btn-success:hover {
        background: #45a049;
      }

      .btn-info {
        background: var(--info-color);
        color: white;
      }

      .btn-info:hover {
        background: #1976d2;
      }

      .btn-excel {
        background: #217346;
        color: white;
      }

      .btn-excel:hover {
        background: #1a5c38;
      }

      .btn-print {
        background: #607d8b;
        color: white;
      }

      .btn-print:hover {
        background: #546e7a;
      }

      /* ==================== الرأس ==================== */
      .header {
        background: linear-gradient(
          135deg,
          var(--secondary-color),
          var(--primary-color)
        );
        color: white;
        padding: 20px;
        border-radius: 10px;
        margin-bottom: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
      }

      .header .header-logo {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        object-fit: cover;
        border: 2px solid white;
        margin-left: 15px;
        transition: transform 0.3s ease;
      }

      .header .header-logo:hover {
        transform: scale(1.1);
      }

      .header-content {
        display: flex;
        align-items: center;
      }

      .header h1 {
        font-size: 24px;
        text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
      }

      .header-info {
        display: flex;
        gap: 15px;
        align-items: center;
        flex-wrap: wrap;
      }

      .header-info span {
        font-size: 14px;
        background: rgba(255, 255, 255, 0.2);
        padding: 5px 10px;
        border-radius: 20px;
      }

      .save-indicator {
        display: flex;
        align-items: center;
        gap: 8px;
        font-size: 12px;
        padding: 8px 15px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 20px;
      }

      .save-dot {
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: #4caf50;
        animation: pulse 2s infinite;
      }

      @keyframes pulse {
        0%,
        100% {
          opacity: 1;
        }
        50% {
          opacity: 0.5;
        }
      }

      .logout-btn {
        background: rgba(255, 255, 255, 0.2);
        border: 2px solid white;
        color: white;
        padding: 8px 15px;
        border-radius: 20px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
      }

      .logout-btn:hover {
        background: rgba(255, 255, 255, 0.3);
        transform: translateY(-2px);
      }

      /* ==================== مبيعات اليوم في الكاشير ==================== */
      .today-stats {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      .stat-card {
        background: white;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        text-align: center;
        transition: transform 0.3s ease;
      }

      .stat-card:hover {
        transform: translateY(-5px);
      }

      .stat-card h3 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 14px;
      }

      .stat-amount {
        font-size: 24px;
        font-weight: bold;
      }

      .sales-amount {
        color: var(--success-color);
      }

      .expenses-amount {
        color: var(--error-color);
      }

      .net-amount {
        color: var(--info-color);
      }

      /* ==================== شريط البحث ==================== */
      .search-container {
        margin-bottom: 20px;
        position: relative;
      }

      .search-input {
        width: 100%;
        padding: 12px 45px 12px 15px;
        border: 2px solid var(--border-color);
        border-radius: 25px;
        font-size: 14px;
        text-align: right;
        transition: all 0.3s;
      }

      .search-input:focus {
        outline: none;
        border-color: var(--secondary-color);
        box-shadow: 0 0 10px rgba(255, 107, 53, 0.2);
      }

      .search-icon {
        position: absolute;
        left: 15px;
        top: 50%;
        transform: translateY(-50%);
        color: #999;
      }

      /* ==================== واجهة الكاشير ==================== */

      /* قائمة المنتجات - القسم الأيسر */
      .cashier-container > div:first-child {
        flex: 1;
        overflow-y: auto;
        padding-right: 10px;
        max-height: 100%;
        position: relative;
        z-index: 1; /* أقل من الفاتورة */
      }

      /* إضافة خلفية شبه شفافة للفاتورة */
      .invoice-panel::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: rgba(255, 255, 255, 0.95);
        z-index: -1;
        border-radius: 10px;
      }

      /* تحسين ظهور الفاتورة */
      .invoice-header {
        background: linear-gradient(
          135deg,
          var(--secondary-color),
          var(--primary-color)
        );
        color: white;
        padding: 15px;
        border-radius: 10px 10px 0 0;
        text-align: center;
        font-weight: bold;
        font-size: 18px;
        position: sticky;
        top: 0;
        z-index: 11; /* أعلى من محتوى الفاتورة */
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      }

      /* جعل عناصر الفاتورة واضحة */
      .invoice-items {
        flex: 1;
        overflow-y: auto;
        padding: 15px;
        border-bottom: 1px solid var(--border-color);
        background: rgba(255, 255, 255, 0.9);
        position: relative;
        z-index: 9;
      }

      /* تحسين ظهور عناصر الفاتورة */
      .invoice-item {
        background: #f9f9f9;
        padding: 10px;
        margin-bottom: 10px;
        border-radius: 8px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-left: 4px solid var(--secondary-color);
        animation: slideInFromRight 0.4s ease-out;
        position: relative;
        z-index: 9;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      }

      /* إضافة تأثير hover للعناصر */
      .invoice-item:hover {
        transform: translateX(-5px);
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
        z-index: 12;
      }

      /* قسم الإجمالي */
      .invoice-total {
        padding: 15px;
        text-align: center;
        border-bottom: 2px solid var(--primary-color);
        background: rgba(255, 255, 255, 0.95);
        position: sticky;
        bottom: 0;
        z-index: 11;
        box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
      }

      /* قسم طرق الدفع */
      .payment-methods {
        padding: 15px;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        border-bottom: 1px solid var(--border-color);
        background: rgba(255, 255, 255, 0.95);
        position: relative;
        z-index: 9;
      }

      /* قسم الأزرار */
      .invoice-actions {
        padding: 15px;
        display: flex;
        gap: 10px;
        background: rgba(255, 255, 255, 0.95);
        position: relative;
        z-index: 9;
        border-radius: 0 0 10px 10px;
      }

      /* تحسين شريط التمرير */
      .cashier-container > div:first-child::-webkit-scrollbar,
      .invoice-panel::-webkit-scrollbar {
        width: 8px;
      }

      .cashier-container > div:first-child::-webkit-scrollbar-track,
      .invoice-panel::-webkit-scrollbar-track {
        background: #f1f1f1;
        border-radius: 10px;
      }

      .cashier-container > div:first-child::-webkit-scrollbar-thumb,
      .invoice-panel::-webkit-scrollbar-thumb {
        background: #888;
        border-radius: 10px;
      }

      .cashier-container > div:first-child::-webkit-scrollbar-thumb:hover,
      .invoice-panel::-webkit-scrollbar-thumb:hover {
        background: #555;
      }

      /* للشاشات الصغيرة */
      @media (max-width: 768px) {
        .cashier-container {
          flex-direction: column;
          height: auto;
        }

        .invoice-panel {
          width: 100%;
          flex-shrink: 0;
          background: white;
          border-radius: 10px;
          box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
          display: flex;
          flex-direction: column;
          position: relative;
          top: 0;
          margin-top: 20px;
          max-height: 80vh; /* 👈 ارتفاع مناسب للشاشات الصغيرة */
          border: 2px solid var(--primary-color);
        }

        .cashier-container > div:first-child {
          max-height: 400px;
          z-index: 1;
        }
      }

      /* ==================== نوع الطلب ==================== */
      .order-type-container {
        margin-bottom: 15px;
        padding: 15px;
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      }

      .order-type-container h3 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 16px;
      }

      .order-type-buttons {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
      }

      .order-type-btn {
        flex: 1;
        min-width: 100px;
        padding: 10px;
        border: 2px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
        text-align: center;
      }

      .order-type-btn.active {
        background: var(--primary-color);
        border-color: var(--secondary-color);
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      }

      .order-type-btn.hall {
        border-color: #4caf50;
      }

      .order-type-btn.takeout {
        border-color: #2196f3;
      }

      .order-type-btn.delivery {
        border-color: #ff9800;
      }

      /* ==================== منطقة التوصيل (جديد) ==================== */
      .delivery-zones-container {
        margin-bottom: 15px;
        padding: 15px;
        background: #fff9e6;
        border-radius: 10px;
        border: 2px solid var(--primary-color);
      }

      .delivery-zones-title {
        font-weight: bold;
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 15px;
      }

      .delivery-zone-buttons {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
      }

      .zone-btn {
        flex: 1 0 calc(33.333% - 10px);
        min-width: 80px;
        padding: 12px 5px;
        border: 2px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.2s;
        font-size: 14px;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .zone-btn.active {
        background: var(--secondary-color);
        border-color: var(--primary-color);
        color: white;
        transform: translateY(-2px);
      }

      .zone-price {
        font-size: 12px;
        color: var(--secondary-color);
        margin-top: 3px;
      }

      .zone-btn.active .zone-price {
        color: white;
      }

      /* ==================== واجهة المدير ==================== */
      .admin-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
      }

      .panel {
        background: white;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
      }

      .panel:hover {
        transform: translateY(-2px);
      }

      /* تنسيق أدوات البنل (العنوان + الأزرار) */
      .panel-header-tools {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
        flex-wrap: wrap;
        gap: 10px;
      }

      .panel-header-tools h2,
      .panel-header-tools h3 {
        margin: 0;
        color: var(--secondary-color);
      }

      .panel h2 {
        color: var(--secondary-color);
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .panel h3 {
        color: var(--text-dark);
        margin-top: 15px;
        margin-bottom: 10px;
        font-size: 16px;
      }

      .form-group-inline {
        display: flex;
        gap: 10px;
        margin-bottom: 15px;
        flex-wrap: wrap;
      }

      .form-group-inline input,
      .form-group-inline select {
        flex: 1;
        min-width: 150px;
        padding: 10px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
      }

      .form-group-inline button {
        padding: 10px 20px;
      }

      /* ==================== جدول المنتجات ==================== */
      .products-table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 15px;
        font-size: 14px;
      }

      .products-table th {
        background: var(--primary-color);
        color: var(--text-dark);
        padding: 12px;
        text-align: right;
        font-weight: bold;
        border: 1px solid var(--border-color);
      }

      .products-table td {
        padding: 12px;
        border: 1px solid var(--border-color);
        text-align: right;
      }

      .products-table tr:nth-child(even) {
        background: #f9f9f9;
      }

      .products-table tr:hover {
        background: #f0f0f0;
      }

      .product-img {
        width: 50px;
        height: 50px;
        object-fit: cover;
        border-radius: 8px;
      }

      .action-btns {
        display: flex;
        gap: 5px;
        justify-content: flex-end;
      }

      .action-btns button {
        padding: 5px 10px;
        font-size: 12px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .edit-btn {
        background: var(--warning-color);
        color: white;
      }

      .delete-btn {
        background: var(--error-color);
        color: white;
      }

      /* ==================== واجهة الكاشير ==================== */
      .cashier-container {
        display: grid;
        grid-template-columns: 2fr 1fr;
        gap: 20px;
      }

      .products-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 15px;
      }

      .product-card {
        background: white;
        border: 2px solid var(--border-color);
        border-radius: 10px;
        padding: 15px;
        text-align: center;
        cursor: pointer;
        transition: all 0.3s;
        display: flex;
        flex-direction: column;
      }

      .product-card:hover {
        border-color: var(--secondary-color);
        box-shadow: 0 5px 15px rgba(255, 107, 53, 0.2);
        transform: translateY(-5px);
      }

      .product-card img {
        width: 100%;
        height: 120px;
        object-fit: cover;
        border-radius: 8px;
        margin-bottom: 10px;
      }

      .product-card h4 {
        color: var(--text-dark);
        margin-bottom: 8px;
        font-size: 14px;
      }

      .product-card .price {
        color: var(--secondary-color);
        font-size: 18px;
        font-weight: bold;
        margin-bottom: 10px;
      }

      .product-card .add-btn {
        background: var(--primary-color);
        color: var(--text-dark);
        border: none;
        padding: 8px;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
        margin-top: auto;
      }

      .product-card .add-btn:hover {
        background: #ffc700;
        transform: translateY(-2px);
      }

      .invoice-header {
        background: var(--primary-color);
        color: var(--text-dark);
        padding: 15px;
        border-radius: 10px 10px 0 0;
        text-align: center;
        font-weight: bold;
        font-size: 18px;
      }

      .invoice-items {
        flex: 1;
        padding: 15px;
        border-bottom: 1px solid var(--border-color);
      }

      .invoice-item {
        background: #f9f9f9;
        padding: 10px;
        margin-bottom: 10px;
        border-radius: 8px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-left: 4px solid var(--secondary-color);
        animation: slideInFromRight 0.4s ease-out;
      }

      @keyframes slideInFromRight {
        from {
          opacity: 0;
          transform: translateX(30px);
        }
        to {
          opacity: 1;
          transform: translateX(0);
        }
      }

      .invoice-item-info {
        flex: 1;
      }

      .invoice-item-name {
        font-weight: bold;
        color: var(--text-dark);
      }

      .invoice-item-qty {
        font-size: 12px;
        color: #666;
        display: flex;
        align-items: center;
        gap: 5px;
      }

      .invoice-item-price {
        color: var(--secondary-color);
        font-weight: bold;
      }

      .invoice-item-remove {
        background: var(--error-color);
        color: white;
        border: none;
        padding: 5px 10px;
        border-radius: 5px;
        cursor: pointer;
        font-size: 12px;
      }

      .invoice-total {
        padding: 15px;
        text-align: center;
        border-bottom: 2px solid var(--primary-color);
      }

      .invoice-total-label {
        font-size: 14px;
        color: #666;
      }

      .invoice-total-amount {
        font-size: 28px;
        font-weight: bold;
        color: var(--secondary-color);
      }

      .payment-methods {
        padding: 15px;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        border-bottom: 1px solid var(--border-color);
      }

      .payment-btn {
        padding: 10px;
        border: 2px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
        font-size: 12px;
      }

      .payment-btn.active {
        background: var(--primary-color);
        border-color: var(--secondary-color);
      }

      .invoice-actions {
        padding: 15px;
        display: flex;
        gap: 10px;
      }

      .invoice-actions button {
        flex: 1;
        padding: 12px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
      }

      .empty-state {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 40px 20px;
        color: #999;
      }

      .empty-state-icon {
        font-size: 48px;
        margin-bottom: 10px;
      }

      /* ==================== صرف المصاريف ==================== */
      .expense-card {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        margin-bottom: 20px;
      }

      .expense-form {
        display: grid;
        grid-template-columns: 2fr 1fr 1fr;
        gap: 10px;
        align-items: end;
      }

      .expense-list {
        margin-top: 20px;
      }

      .expense-item {
        background: #fff3e0;
        padding: 10px;
        margin-bottom: 10px;
        border-radius: 8px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-right: 4px solid var(--error-color);
      }

      .expense-item-info {
        flex: 1;
      }

      .expense-item-description {
        font-weight: bold;
        color: var(--text-dark);
      }

      .expense-item-date {
        font-size: 12px;
        color: #666;
      }

      .expense-item-amount {
        color: var(--error-color);
        font-weight: bold;
      }

      /* ==================== نافذة اختيار الكمية ==================== */
      .quantity-modal-overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1000;
      }

      .quantity-modal {
        background: white;
        border-radius: 15px;
        width: 90%;
        max-width: 400px;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        overflow: hidden;
        animation: modalAppear 0.3s ease-out;
      }

      @keyframes modalAppear {
        from {
          opacity: 0;
          transform: scale(0.8) translateY(-20px);
        }
        to {
          opacity: 1;
          transform: scale(1) translateY(0);
        }
      }

      .quantity-modal-header {
        background: linear-gradient(
          135deg,
          var(--secondary-color),
          var(--primary-color)
        );
        color: white;
        padding: 20px;
        text-align: center;
        position: relative;
      }

      .quantity-modal-close {
        position: absolute;
        left: 15px;
        top: 50%;
        transform: translateY(-50%);
        background: rgba(255, 255, 255, 0.2);
        border: none;
        color: white;
        width: 30px;
        height: 30px;
        border-radius: 50%;
        cursor: pointer;
        font-size: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .quantity-modal-product {
        font-size: 18px;
        font-weight: bold;
        margin-bottom: 5px;
      }

      .quantity-modal-price {
        font-size: 14px;
        opacity: 0.9;
      }

      .quantity-display {
        padding: 20px;
        text-align: center;
        border-bottom: 1px solid var(--border-color);
      }

      .quantity-value {
        font-size: 48px;
        font-weight: bold;
        color: var(--secondary-color);
        margin: 10px 0;
        direction: ltr;
        text-align: center;
      }

      .quantity-max-notice {
        font-size: 12px;
        color: #999;
        margin-top: 5px;
      }

      .quantity-keypad {
        padding: 20px;
      }

      .quantity-buttons-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        margin-bottom: 15px;
      }

      .quantity-btn {
        background: white;
        border: 2px solid var(--border-color);
        border-radius: 10px;
        padding: 15px 10px;
        font-size: 20px;
        font-weight: bold;
        cursor: pointer;
        transition: all 0.2s;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .quantity-btn:hover {
        background: #f5f5f5;
        transform: translateY(-2px);
      }

      .quantity-btn:active {
        transform: translateY(0);
      }

      .quantity-btn.number {
        color: var(--text-dark);
      }

      .quantity-btn.double-zero {
        color: var(--text-dark);
      }

      .quantity-btn.clear {
        color: var(--error-color);
        border-color: var(--error-color);
      }

      .quantity-btn.backspace {
        color: var(--warning-color);
        border-color: var(--warning-color);
      }

      .quantity-action-buttons {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }

      .quantity-action-btn {
        padding: 15px;
        border: none;
        border-radius: 10px;
        font-size: 16px;
        font-weight: bold;
        cursor: pointer;
        transition: all 0.2s;
      }

      .quantity-cancel-btn {
        background: #f5f5f5;
        color: var(--text-dark);
      }

      .quantity-cancel-btn:hover {
        background: #e0e0e0;
      }

      .quantity-add-btn {
        background: var(--success-color);
        color: white;
      }

      .quantity-add-btn:hover {
        background: #45a049;
        transform: translateY(-2px);
      }

      .quantity-add-btn:disabled {
        background: #cccccc;
        cursor: not-allowed;
        transform: none;
      }

      /* ==================== تقرير نهاية الدوام ==================== */
      .shift-report {
        margin-top: 20px;
      }

      .report-summary {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      .summary-card {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        text-align: center;
      }

      .summary-card h4 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 14px;
      }

      .summary-value {
        font-size: 20px;
        font-weight: bold;
      }

      /* ==================== التبويبات ==================== */
      .tabs {
        display: flex;
        gap: 10px;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--border-color);
        flex-wrap: wrap;
      }

      .tab-btn {
        padding: 12px 20px;
        border: none;
        background: transparent;
        cursor: pointer;
        font-weight: bold;
        color: #666;
        border-bottom: 3px solid transparent;
        transition: all 0.3s;
      }

      .tab-btn.active {
        color: var(--secondary-color);
        border-bottom-color: var(--secondary-color);
      }

      .tab-content {
        display: none;
      }

      .tab-content.active {
        display: block;
      }

      /* ==================== التقارير ==================== */
      .report-card {
        background: white;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        margin-bottom: 20px;
      }

      .report-card h3 {
        color: var(--secondary-color);
        margin-bottom: 15px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .report-stat {
        display: flex;
        justify-content: space-between;
        padding: 10px 0;
        border-bottom: 1px solid var(--border-color);
      }

      .report-stat:last-child {
        border-bottom: none;
      }

      .report-stat-label {
        font-weight: bold;
        color: var(--text-dark);
      }

      .report-stat-value {
        color: var(--secondary-color);
        font-weight: bold;
      }

      /* ==================== فلترة التقارير ==================== */
      .report-filter {
        display: flex;
        gap: 10px;
        margin-bottom: 20px;
        flex-wrap: wrap;
        align-items: center;
      }

      .filter-btn {
        padding: 8px 15px;
        border: 1px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .filter-btn.active {
        background: var(--primary-color);
        border-color: var(--secondary-color);
      }

      .export-btn {
        margin-right: auto;
        padding: 8px 15px;
        background: #217346;
        color: white;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
        display: flex;
        align-items: center;
        gap: 5px;
      }

      .export-btn:hover {
        background: #1a5c38;
      }

      /* ==================== نظام فلترة الكاشير ==================== */
      .cashier-report-filter {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        margin-bottom: 20px;
      }

      .filter-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-top: 10px;
      }

      .filter-section {
        display: flex;
        flex-direction: column;
        gap: 8px;
      }

      .filter-section label {
        font-weight: bold;
        color: var(--secondary-color);
        font-size: 14px;
      }

      .filter-section select,
      .filter-section input {
        padding: 8px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
      }

      /* ==================== الإشعارات ==================== */
      .notification {
        position: fixed;
        top: 20px;
        right: 20px;
        padding: 15px 20px;
        border-radius: 8px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        animation: popIn 0.5s ease-out;
        z-index: 2000;
        font-weight: bold;
        max-width: 300px;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .notification.success {
        background: var(--success-color);
        color: white;
      }

      .notification.error {
        background: var(--error-color);
        color: white;
      }

      .notification.warning {
        background: var(--warning-color);
        color: white;
      }

      .notification.info {
        background: var(--info-color);
        color: white;
      }

      @keyframes popIn {
        0% {
          opacity: 0;
          transform: translateY(-20px) scale(0.9);
        }
        70% {
          transform: translateY(5px) scale(1.02);
        }
        100% {
          opacity: 1;
          transform: translateY(0) scale(1);
        }
      }

      /* ==================== الشاشات ==================== */
      #loginScreen {
        display: flex;
      }

      #cashierScreen,
      #adminScreen {
        display: none;
      }

      .hidden {
        display: none !important;
      }

      /* ==================== ميزات جديدة ==================== */

      /* لوحة التحكم الشاملة للمدير */
      .dashboard-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-bottom: 30px;
      }

      .dashboard-card {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        transition: transform 0.3s;
      }

      .dashboard-card:hover {
        transform: translateY(-5px);
      }

      .dashboard-card-header {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
      }

      .dashboard-card-icon {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-left: 15px;
        font-size: 18px;
      }

      .dashboard-card-icon.sales {
        background: rgba(76, 175, 80, 0.2);
        color: var(--success-color);
      }

      .dashboard-card-icon.orders {
        background: rgba(33, 150, 243, 0.2);
        color: var(--info-color);
      }

      .dashboard-card-icon.products {
        background: rgba(255, 152, 0, 0.2);
        color: var(--warning-color);
      }

      .dashboard-card-icon.expenses {
        background: rgba(244, 67, 54, 0.2);
        color: var(--error-color);
      }

      .dashboard-card-title {
        font-size: 16px;
        color: #666;
      }

      .dashboard-card-value {
        font-size: 28px;
        font-weight: bold;
        color: var(--text-dark);
      }

      .dashboard-card-change {
        font-size: 14px;
        margin-top: 10px;
        display: flex;
        align-items: center;
      }

      .dashboard-card-change.positive {
        color: var(--success-color);
      }

      .dashboard-card-change.negative {
        color: var(--error-color);
      }

      /* إدارة الطلبات */
      .orders-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
        margin-bottom: 20px;
      }

      .order-card {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        transition: transform 0.3s;
      }

      .order-card:hover {
        transform: translateY(-5px);
      }

      .order-card-header {
        padding: 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid var(--border-color);
      }

      .order-card-number {
        font-weight: bold;
        font-size: 16px;
        color: var(--text-dark);
      }

      .order-card-status {
        padding: 5px 10px;
        border-radius: 20px;
        font-size: 12px;
        font-weight: bold;
        color: white;
      }

      .order-card-status.pending {
        background: var(--order-pending);
      }

      .order-card-status.preparing {
        background: var(--order-preparing);
      }

      .order-card-status.ready {
        background: var(--order-ready);
      }

      .order-card-status.delivered {
        background: var(--order-delivered);
      }

      .order-card-body {
        padding: 15px;
      }

      .order-card-info {
        display: flex;
        justify-content: space-between;
        margin-bottom: 10px;
        font-size: 14px;
      }

      .order-card-items {
        margin-bottom: 15px;
      }

      .order-card-item {
        display: flex;
        justify-content: space-between;
        padding: 5px 0;
        font-size: 14px;
        border-bottom: 1px solid #f0f0f0;
      }

      .order-card-total {
        font-weight: bold;
        text-align: right;
        font-size: 16px;
        margin-top: 10px;
      }

      .order-card-actions {
        padding: 10px 15px;
        background: #f9f9f9;
        display: flex;
        gap: 10px;
      }

      .order-card-actions button {
        flex: 1;
        padding: 8px;
        border: none;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .order-card-actions .btn-view {
        background: var(--info-color);
        color: white;
      }

      .order-card-actions .btn-complete {
        background: var(--success-color);
        color: white;
      }

      /* إدارة المرتجعات */
      .returns-container {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .returns-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 1px solid var(--border-color);
        padding-bottom: 10px;
      }

      .returns-table {
        width: 100%;
        border-collapse: collapse;
      }

      .returns-table th {
        background: #f9f9f9;
        padding: 10px;
        text-align: right;
        font-weight: bold;
        border-bottom: 1px solid var(--border-color);
      }

      .returns-table td {
        padding: 10px;
        border-bottom: 1px solid var(--border-color);
      }

      .returns-table tr:hover {
        background: #f9f9f9;
      }

      .return-reason {
        font-size: 12px;
        color: #666;
        max-width: 200px;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }

      /* تحسينات الفاتورة */
      .invoice-options {
        padding: 15px;
        border-bottom: 1px solid var(--border-color);
      }

      .invoice-options-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }

      .invoice-option {
        display: flex;
        flex-direction: column;
        gap: 5px;
      }

      .invoice-option label {
        font-size: 12px;
        font-weight: bold;
        color: #666;
      }

      .invoice-option input,
      .invoice-option select,
      .invoice-option textarea {
        padding: 8px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
      }

      .invoice-discount {
        display: flex;
        align-items: center;
        gap: 10px;
        padding: 10px 15px;
        border-bottom: 1px solid var(--border-color);
      }

      .invoice-discount label {
        font-size: 14px;
        font-weight: bold;
      }

      .invoice-discount input {
        width: 80px;
        padding: 5px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        text-align: center;
      }

      .invoice-discount-type {
        display: flex;
        gap: 5px;
      }

      .discount-type-btn {
        padding: 5px 10px;
        border: 1px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-size: 12px;
      }

      .discount-type-btn.active {
        background: var(--primary-color);
        border-color: var(--secondary-color);
      }

      .invoice-notes {
        padding: 10px 15px;
        border-bottom: 1px solid var(--border-color);
      }

      .invoice-notes label {
        display: block;
        font-size: 14px;
        font-weight: bold;
        margin-bottom: 5px;
      }

      .invoice-notes textarea {
        width: 100%;
        padding: 8px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
        resize: none;
        min-height: 60px;
      }

      /* تحسينات إدخال الكمية */
      .quick-quantity-buttons {
        display: flex;
        gap: 10px;
        margin-top: 10px;
      }

      .quick-quantity-btn {
        flex: 1;
        padding: 10px;
        border: 2px solid var(--border-color);
        background: white;
        border-radius: 8px;
        cursor: pointer;
        font-weight: bold;
        transition: all 0.3s;
      }

      .quick-quantity-btn:hover {
        background: var(--primary-color);
        border-color: var(--secondary-color);
      }

      /* المنتجات الأكثر مبيعاً */
      .top-products-section {
        margin-bottom: 20px;
      }

      .top-products-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
      }

      .top-products-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
        gap: 15px;
      }

      .top-product-card {
        background: white;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        padding: 15px;
        text-align: center;
        cursor: pointer;
        transition: all 0.3s;
      }

      .top-product-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
      }

      .top-product-rank {
        background: var(--secondary-color);
        color: white;
        width: 24px;
        height: 24px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        font-size: 12px;
        margin: 0 auto 10px;
      }

      .top-product-name {
        font-size: 14px;
        font-weight: bold;
        margin-bottom: 5px;
        color: var(--text-dark);
      }

      .top-product-count {
        font-size: 12px;
        color: #666;
      }

      /* مؤشرات الحالة */
      .sync-indicator {
        display: flex;
        align-items: center;
        gap: 8px;
        font-size: 12px;
        padding: 8px 15px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 20px;
      }

      .sync-pending-badge {
        background: #ff9800;
        color: white;
        padding: 2px 6px;
        border-radius: 10px;
        font-size: 10px;
        margin-right: 5px;
        display: none;
      }

      /* إدارة الأقسام */
      .categories-management {
        margin-bottom: 20px;
      }

      .category-list {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 15px;
      }

      .category-tag {
        background: var(--primary-color);
        color: var(--text-dark);
        padding: 8px 15px;
        border-radius: 20px;
        font-weight: bold;
        display: flex;
        align-items: center;
        gap: 8px;
      }

      .category-tag button {
        background: none;
        border: none;
        color: var(--text-dark);
        cursor: pointer;
        font-size: 16px;
        padding: 0;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .category-tag button:hover {
        background: rgba(0, 0, 0, 0.1);
      }

      .add-category-form {
        display: flex;
        gap: 10px;
      }

      .add-category-form input {
        flex: 1;
        padding: 10px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        text-align: right;
      }

      /* إدارة أرقام التوصيل */
      .delivery-numbers-management {
        margin-bottom: 20px;
      }

      .delivery-numbers-list {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 15px;
      }

      .delivery-number-tag {
        background: var(--info-color);
        color: white;
        padding: 8px 15px;
        border-radius: 20px;
        font-weight: bold;
        display: flex;
        align-items: center;
        gap: 8px;
      }

      .delivery-number-tag button {
        background: none;
        border: none;
        color: white;
        cursor: pointer;
        font-size: 16px;
        padding: 0;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .delivery-number-tag button:hover {
        background: rgba(255, 255, 255, 0.2);
      }

      .add-delivery-number-form {
        display: flex;
        gap: 10px;
        margin-bottom: 10px;
      }

      .add-delivery-number-form input {
        flex: 1;
        padding: 10px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        text-align: right;
      }

      /* واجهة الدليفري */
      .delivery-container {
        display: grid;
        grid-template-columns: 1fr;
        gap: 20px;
      }

      .delivery-orders-container {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
      }

      .delivery-order-card {
        background: #f9f9f9;
        border-radius: 10px;
        padding: 15px;
        margin-bottom: 15px;
        border-left: 4px solid var(--info-color);
      }

      .delivery-order-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
      }

      .delivery-order-number {
        font-weight: bold;
        font-size: 16px;
        color: var(--text-dark);
      }

      .delivery-order-status {
        padding: 5px 10px;
        border-radius: 20px;
        font-size: 12px;
        font-weight: bold;
        color: white;
      }

      .delivery-order-status.pending {
        background: var(--order-pending);
      }

      .delivery-order-status.delivered {
        background: var(--order-delivered);
      }

      .delivery-order-info {
        display: flex;
        justify-content: space-between;
        margin-bottom: 10px;
        font-size: 14px;
      }

      .delivery-order-customer {
        font-weight: bold;
        color: var(--text-dark);
      }

      .delivery-order-address {
        color: #666;
        font-size: 14px;
        margin-bottom: 10px;
      }

      .delivery-order-actions {
        display: flex;
        gap: 10px;
      }

      .delivery-order-actions button {
        flex: 1;
        padding: 8px;
        border: none;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .delivery-order-actions .btn-view {
        background: var(--info-color);
        color: white;
      }

      .delivery-order-actions .btn-deliver {
        background: var(--success-color);
        color: white;
      }

      .delivery-stats {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      .delivery-stat-card {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        text-align: center;
      }

      .delivery-stat-card h3 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 14px;
      }

      .delivery-stat-amount {
        font-size: 22px;
        font-weight: bold;
      }

      /* منطقة اختيار مكان التوصيل في الفاتورة */
      .delivery-location-section {
        padding: 10px 15px;
        border-bottom: 1px solid var(--border-color);
        display: none;
      }

      .delivery-location-section.active {
        display: block;
      }

      .delivery-location-input {
        width: 100%;
        padding: 8px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
        margin-bottom: 10px;
      }

      /* تحسينات قائمة المستخدمين */
      .users-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
      }

      .user-card {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        transition: transform 0.3s;
      }

      .user-card:hover {
        transform: translateY(-5px);
      }

      .user-card-header {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
      }

      .user-avatar {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background: var(--primary-color);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 20px;
        color: white;
        margin-left: 15px;
      }

      .user-info h3 {
        margin: 0;
        color: var(--text-dark);
      }

      .user-info p {
        margin: 5px 0 0;
        color: #666;
        font-size: 14px;
      }

      .user-role {
        display: inline-block;
        padding: 5px 10px;
        border-radius: 20px;
        font-size: 12px;
        font-weight: bold;
        color: white;
        margin-bottom: 10px;
      }

      .user-role.admin {
        background: var(--admin-color);
      }

      .user-role.cashier {
        background: var(--cashier-color);
      }

      .user-actions {
        display: flex;
        gap: 10px;
        margin-top: 15px;
      }

      .user-actions button {
        flex: 1;
        padding: 8px;
        border: none;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .user-actions .edit-btn {
        background: var(--warning-color);
        color: white;
      }

      .user-actions .delete-btn {
        background: var(--error-color);
        color: white;
      }

      /* تحسينات النسخ الاحتياطي */
      .backup-options {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-bottom: 20px;
      }

      .backup-option {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        text-align: center;
        transition: transform 0.3s;
      }

      .backup-option:hover {
        transform: translateY(-5px);
      }

      .backup-option i {
        font-size: 40px;
        margin-bottom: 15px;
        color: var(--secondary-color);
      }

      .backup-option h3 {
        margin-bottom: 10px;
        color: var(--text-dark);
      }

      .backup-option p {
        color: #666;
        margin-bottom: 15px;
      }

      .backup-option button {
        width: 100%;
      }

      /* تحسينات الطباعة */
      .print-preview {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.8);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 2000;
      }

      .print-preview-content {
        background: white;
        width: 80%;
        max-width: 800px;
        height: 80%;
        border-radius: 10px;
        overflow: hidden;
        display: flex;
        flex-direction: column;
      }

      .print-preview-header {
        background: var(--secondary-color);
        color: white;
        padding: 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }

      .print-preview-body {
        flex: 1;
        overflow: auto;
        padding: 20px;
      }

      .print-preview-footer {
        padding: 15px;
        border-top: 1px solid var(--border-color);
        display: flex;
        justify-content: flex-end;
        gap: 10px;
      }

      /* ==================== نظام الموظفين ==================== */
      .employees-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
        margin-bottom: 20px;
      }

      .employee-card {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        transition: transform 0.3s;
      }

      .employee-card:hover {
        transform: translateY(-5px);
      }

      .employee-card-header {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
      }

      .employee-avatar {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        background: linear-gradient(
          135deg,
          var(--secondary-color),
          var(--primary-color)
        );
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 24px;
        color: white;
        margin-left: 15px;
      }

      .employee-info h3 {
        margin: 0;
        color: var(--text-dark);
        font-size: 18px;
      }

      .employee-info p {
        margin: 5px 0 0;
        color: #666;
        font-size: 14px;
      }

      .employee-details {
        margin: 15px 0;
        padding: 10px;
        background: #f9f9f9;
        border-radius: 8px;
      }

      .employee-detail {
        display: flex;
        justify-content: space-between;
        margin-bottom: 8px;
        font-size: 14px;
      }

      .employee-detail:last-child {
        margin-bottom: 0;
      }

      .employee-detail-label {
        font-weight: bold;
        color: var(--text-dark);
      }

      .employee-detail-value {
        color: var(--secondary-color);
      }

      .employee-actions {
        display: flex;
        gap: 10px;
        margin-top: 15px;
        flex-wrap: wrap;
      }

      .employee-actions button {
        flex: 1;
        min-width: 120px;
        padding: 8px;
        border: none;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .employee-actions .btn-loan {
        background: #9c27b0;
        color: white;
      }

      .employee-actions .btn-vacation {
        background: #2196f3;
        color: white;
      }

      .employee-actions .btn-deduction {
        background: #ff9800;
        color: white;
      }

      .employee-actions .btn-salary {
        background: #4caf50;
        color: white;
      }

      .employee-actions .btn-print {
        background: #607d8b;
        color: white;
      }

      /* ==================== طباعة تقرير الموظف ==================== */
      .print-employee-btn {
        background: #607d8b;
        color: white;
        padding: 8px 15px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 12px;
        transition: all 0.3s;
        display: flex;
        align-items: center;
        gap: 5px;
      }

      .print-employee-btn:hover {
        background: #546e7a;
        transform: translateY(-2px);
      }

      /* ==================== إدارة الطاولات ==================== */
      .tables-container {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .tables-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .tables-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
        gap: 15px;
      }

      .table-card {
        background: #f9f9f9;
        border: 2px solid var(--border-color);
        border-radius: 10px;
        padding: 15px;
        text-align: center;
        cursor: pointer;
        transition: all 0.3s;
      }

      .table-card:hover {
        border-color: var(--secondary-color);
        box-shadow: 0 5px 15px rgba(255, 107, 53, 0.2);
        transform: translateY(-5px);
      }

      .table-card.occupied {
        background: #ffebee;
        border-color: var(--error-color);
      }

      .table-card.selected {
        background: #e8f5e9;
        border-color: var(--success-color);
      }

      .table-number {
        font-size: 24px;
        font-weight: bold;
        color: var(--text-dark);
        margin-bottom: 5px;
      }

      .table-status {
        font-size: 12px;
        color: #666;
      }

      .table-card.occupied .table-status {
        color: var(--error-color);
      }

      .table-card.selected .table-status {
        color: var(--success-color);
      }

      .table-section {
        margin-bottom: 15px;
      }

      .table-section-title {
        font-size: 16px;
        font-weight: bold;
        color: var(--secondary-color);
        margin-bottom: 10px;
        border-bottom: 1px solid var(--border-color);
        padding-bottom: 5px;
      }

      /* إدارة معلومات المطعم */
      .restaurant-info-management {
        margin-bottom: 20px;
      }

      .info-form {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 15px;
        margin-bottom: 15px;
      }

      .info-form .form-group {
        margin-bottom: 15px;
      }

      /* ==================== قسم أسعار التوصيل (جديد) ==================== */
      .delivery-prices-section {
        margin: 20px 0;
        padding: 15px;
        background: #f9f9f9;
        border-radius: 10px;
        border: 1px solid var(--border-color);
      }

      .delivery-prices-section h3 {
        color: var(--secondary-color);
        margin-bottom: 15px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 5px;
      }

      .delivery-prices-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        gap: 15px;
      }

      .price-input label {
        font-size: 14px;
        font-weight: bold;
        display: block;
        margin-bottom: 5px;
      }

      .price-input input {
        width: 100%;
        padding: 8px;
        border: 1px solid var(--border-color);
        border-radius: 5px;
        text-align: center;
        direction: ltr;
      }

      /* ==================== قسم المكونات اليدوية ==================== */
      .product-ingredients-manual {
        margin-top: 15px;
        padding: 15px;
        background: #f9f9f9;
        border-radius: 8px;
      }

      .product-ingredients-manual-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
        border-bottom: 1px solid var(--border-color);
        padding-bottom: 10px;
      }

      .product-ingredients-manual-list {
        margin-bottom: 15px;
      }

      .product-ingredient-manual-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 8px;
        margin-bottom: 5px;
        background: white;
        border-radius: 5px;
        border: 1px solid var(--border-color);
      }

      .product-ingredient-manual-name {
        font-weight: bold;
        color: var(--text-dark);
      }

      .product-ingredient-manual-quantity {
        color: var(--secondary-color);
        font-weight: bold;
      }

      .add-product-ingredient-manual-form {
        display: grid;
        grid-template-columns: 2fr 1fr 1fr 1fr;
        gap: 10px;
      }

      .ingredient-unit-select {
        padding: 10px;
        border: 1px solid var(--border-color);
        border-radius: 8px;
        font-size: 14px;
        text-align: right;
      }

      /* ==================== قسم مبيعات المنتجات والمكونات ==================== */
      .product-sales-container {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .product-sales-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .product-sales-filter {
        display: flex;
        gap: 10px;
        margin-bottom: 20px;
        flex-wrap: wrap;
      }

      .product-sales-table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 15px;
        font-size: 14px;
      }

      .product-sales-table th {
        background: var(--info-color);
        color: white;
        padding: 12px;
        text-align: right;
        font-weight: bold;
        border: 1px solid var(--border-color);
      }

      .product-sales-table td {
        padding: 12px;
        border: 1px solid var(--border-color);
        text-align: right;
      }

      .product-sales-table tr:nth-child(even) {
        background: #f9f9f9;
      }

      .product-sales-table tr:hover {
        background: #f0f0f0;
      }

      .product-sales-amount {
        font-weight: bold;
        color: var(--info-color);
      }

      /* ==================== نظام فلترة المبيعات والمصاريف ==================== */
      .sales-filter-section {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .sales-filter-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .sales-filter-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 15px;
      }

      .expenses-filter-section {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .expenses-filter-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .expenses-filter-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 15px;
      }

      /* تحسينات حالة الاتصال */
      .connection-status {
        display: flex;
        align-items: center;
        gap: 8px;
        font-size: 12px;
        padding: 8px 15px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 20px;
        margin-left: 10px;
      }

      .connection-dot {
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: #f44336;
        animation: pulse 2s infinite;
      }

      .connection-dot.online {
        background: #4caf50;
      }

      .connection-dot.offline {
        background: #f44336;
      }

      .connection-text {
        font-size: 12px;
        color: white;
      }

      /* ==================== تحسينات التقارير المفصلة حسب الأقسام ==================== */
      .category-report-section {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        padding: 20px;
        margin-bottom: 20px;
      }

      .category-report-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        border-bottom: 2px solid var(--primary-color);
        padding-bottom: 10px;
      }

      .category-report-table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 15px;
        font-size: 14px;
      }

      .category-report-table th {
        background: var(--primary-color);
        color: var(--text-dark);
        padding: 12px;
        text-align: right;
        font-weight: bold;
        border: 1px solid var(--border-color);
      }

      .category-report-table td {
        padding: 12px;
        border: 1px solid var(--border-color);
        text-align: right;
      }

      .category-report-table tr:nth-child(even) {
        background: #f9f9f9;
      }

      .category-report-table tr:hover {
        background: #f0f0f0;
      }

      .category-name-cell {
        font-weight: bold;
        background-color: #f0f8ff;
        border-bottom: 2px solid var(--primary-color);
      }

      .category-total-row {
        font-weight: bold;
        background-color: #f0f8ff;
      }

      .category-report-summary {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      .category-summary-card {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        text-align: center;
      }

      .category-summary-card h4 {
        color: var(--secondary-color);
        margin-bottom: 10px;
        font-size: 14px;
      }

      .category-summary-value {
        font-size: 20px;
        font-weight: bold;
      }

      .category-sales-amount {
        color: var(--success-color);
      }

      .category-expenses-amount {
        color: var(--error-color);
      }

      .category-net-amount {
        color: var(--info-color);
      }

      /* ==================== تعليق الفاتورة ==================== */
      .hold-invoices-section {
        margin-bottom: 20px;
        display: none;
      }

      .hold-invoices-section.active {
        display: block;
      }

      .hold-invoices-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
        background: var(--hold-color);
        color: white;
        padding: 10px 15px;
        border-radius: 10px;
      }

      .hold-invoices-header h3 {
        margin: 0;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .hold-invoices-count {
        background: rgba(255, 255, 255, 0.3);
        padding: 3px 10px;
        border-radius: 20px;
        font-size: 14px;
      }

      .hold-invoices-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      .hold-invoice-card {
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        transition: transform 0.3s;
        border-left: 4px solid var(--hold-color);
      }

      .hold-invoice-card:hover {
        transform: translateY(-5px);
      }

      .hold-invoice-header {
        background: rgba(156, 39, 176, 0.1);
        padding: 10px 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }

      .hold-invoice-number {
        font-weight: bold;
        color: var(--hold-color);
      }

      .hold-invoice-time {
        font-size: 12px;
        color: #666;
      }

      .hold-invoice-body {
        padding: 15px;
      }

      .hold-invoice-items {
        margin-bottom: 10px;
      }

      .hold-invoice-item {
        display: flex;
        justify-content: space-between;
        padding: 5px 0;
        font-size: 14px;
        border-bottom: 1px dashed #eee;
      }

      .hold-invoice-item:last-child {
        border-bottom: none;
      }

      .hold-invoice-item-name {
        font-weight: bold;
      }

      .hold-invoice-item-quantity {
        color: #666;
        margin-left: 5px;
      }

      .hold-invoice-item-price {
        color: var(--secondary-color);
      }

      .hold-invoice-footer {
        padding: 10px 15px;
        background: #f9f9f9;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }

      .hold-invoice-total {
        font-weight: bold;
        color: var(--secondary-color);
      }

      .hold-invoice-actions {
        display: flex;
        gap: 5px;
      }

      .hold-invoice-actions button {
        padding: 5px 10px;
        border: none;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: all 0.3s;
      }

      .hold-invoice-actions .btn-resume {
        background: var(--success-color);
        color: white;
      }

      .hold-invoice-actions .btn-delete {
        background: var(--error-color);
        color: white;
      }

      .btn-hold {
        background: var(--hold-color);
        color: white;
      }

      .btn-hold:hover {
        background: #7b1fa2;
        transform: translateY(-2px);
      }

      .empty-hold-invoices {
        grid-column: 1 / -1;
        text-align: center;
        padding: 30px;
        color: #999;
        font-style: italic;
      }

      @media (max-width: 768px) {
        .admin-container,
        .cashier-container,
        .delivery-container {
          grid-template-columns: 1fr;
        }

        .products-grid {
          grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
        }

        .payment-methods {
          grid-template-columns: 1fr;
        }

        .expense-form {
          grid-template-columns: 1fr;
        }

        .header-info {
          margin-top: 10px;
          width: 100%;
          justify-content: center;
        }

        .invoice-actions {
          flex-direction: column;
        }

        .order-type-buttons {
          flex-direction: column;
        }

        .filter-grid {
          grid-template-columns: 1fr;
        }

        .dashboard-grid {
          grid-template-columns: 1fr;
        }

        .orders-container {
          grid-template-columns: 1fr;
        }

        .users-container {
          grid-template-columns: 1fr;
        }

        .invoice-options-grid {
          grid-template-columns: 1fr;
        }

        .employees-container {
          grid-template-columns: 1fr;
        }

        .employee-actions {
          flex-direction: column;
        }

        .employee-actions button {
          min-width: 100%;
        }

        .panel-header-tools {
          flex-direction: column;
          align-items: flex-start;
        }

        .panel-header-tools .btn {
          width: 100%;
          margin-top: 5px;
          margin-left: 0;
        }

        .tables-grid {
          grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
        }

        .info-form {
          grid-template-columns: 1fr;
        }

        .add-ingredient-form,
        .add-product-ingredient-form {
          grid-template-columns: 1fr;
        }

        .product-sales-filter {
          flex-direction: column;
        }

        .sales-filter-grid,
        .expenses-filter-grid {
          grid-template-columns: 1fr;
        }

        .add-product-ingredient-manual-form {
          grid-template-columns: 1fr;
        }

        .hold-invoices-container {
          grid-template-columns: 1fr;
        }

        /* تنسيقات إضافية لنظام الموظفين */
        .employee-details-modal {
          padding: 15px;
        }

        .monthly-summary {
          background: #f8f9fa;
          border-radius: 10px;
          padding: 15px;
          margin: 15px 0;
          border: 1px solid #dee2e6;
        }

        .monthly-summary h4 {
          color: var(--secondary-color);
          margin-bottom: 10px;
          border-bottom: 2px solid var(--primary-color);
          padding-bottom: 5px;
        }

        .details-section {
          margin: 15px 0;
          padding: 10px;
          background: white;
          border-radius: 8px;
          border: 1px solid var(--border-color);
        }

        .details-section h5 {
          color: var(--info-color);
          margin-bottom: 8px;
        }

        .details-section ul {
          list-style-type: none;
          padding: 0;
          margin: 0;
        }

        .details-section li {
          padding: 5px 0;
          border-bottom: 1px dashed #eee;
        }

        .details-section li:last-child {
          border-bottom: none;
        }

        .employee-report {
          font-family: Arial, sans-serif;
          line-height: 1.6;
        }

        /* تنسيقات الأزرار الجديدة */
        .btn-info {
          background: var(--info-color);
          color: white;
        }

        .btn-info:hover {
          background: #1976d2;
        }

        .btn-warning {
          background: var(--warning-color);
          color: white;
        }

        .btn-warning:hover {
          background: #f57c00;
        }

        /* أضف هذا في قسم CSS */
        .btn-success-large {
          background: linear-gradient(145deg, #4caf50, #45a049);
          color: white;
          padding: 12px 24px;
          border: none;
          border-radius: 8px;
          font-size: 16px;
          font-weight: bold;
          cursor: pointer;
          transition: all 0.3s ease;
          box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }

        .btn-success-large:hover {
          transform: translateY(-2px);
          box-shadow: 0 6px 20px rgba(76, 175, 80, 0.4);
        }
      }

      /* ==================== الحل النهائي لمشكلة تبويب الدليفري - إضافات جديدة ==================== */

      /* تثبيت التبويبات الرئيسية في مكانها */
      #cashierScreen .tabs {
        position: relative !important;
        z-index: 1000 !important;
        display: flex !important;
        flex-wrap: wrap !important;
        gap: 10px !important;
        margin-bottom: 20px !important;
        background: white !important;
        padding: 10px !important;
        border-radius: 10px !important;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1) !important;
        width: 100% !important;
      }

      /* تثبيت أزرار التبويبات */
      #cashierScreen .tab-btn {
        position: relative !important;
        z-index: 1001 !important;
        flex: 1 !important;
        min-width: 120px !important;
        padding: 12px 20px !important;
        border: none !important;
        background: transparent !important;
        cursor: pointer !important;
        font-weight: bold !important;
        color: #666 !important;
        border-bottom: 3px solid transparent !important;
        transition: all 0.3s !important;
      }

      /* تثبيت محتوى التبويبات */
      #cashierScreen .tab-content {
        position: relative !important;
        z-index: 1 !important;
        display: none !important;
        width: 100% !important;
        background: white !important;
        padding: 20px !important;
        border-radius: 10px !important;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1) !important;
        margin-top: 10px !important;
        border: 1px solid #e0e0e0 !important;
      }

      #cashierScreen .tab-content.active {
        display: block !important;
      }

      /* ==================== تنسيقات خاصة لتبويب الدليفري ==================== */
      #cashierDeliveryTab {
        position: relative !important;
        z-index: 1 !important;
        display: none !important;
        width: 100% !important;
        min-height: 500px !important;
        background: white !important;
        border: 2px solid var(--primary-color) !important;
        border-radius: 10px !important;
        padding: 20px !important;
        margin-top: 10px !important;
      }

      #cashierDeliveryTab.active {
        display: block !important;
      }

      /* إحصائيات الدليفري */
      #cashierDeliveryTab .delivery-stats {
        display: grid !important;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)) !important;
        gap: 15px !important;
        margin-bottom: 20px !important;
      }

      #cashierDeliveryTab .delivery-stat-card {
        background: white !important;
        padding: 20px !important;
        border-radius: 10px !important;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1) !important;
        text-align: center !important;
        border: 1px solid #e0e0e0 !important;
      }

      #cashierDeliveryTab .delivery-stat-card h3 {
        color: var(--secondary-color) !important;
        margin-bottom: 10px !important;
        font-size: 14px !important;
      }

      #cashierDeliveryTab .delivery-stat-amount {
        font-size: 24px !important;
        font-weight: bold !important;
        color: var(--text-dark) !important;
      }

      /* قسم الفلترة */
      #cashierDeliveryTab .cashier-report-filter {
        background: white !important;
        padding: 20px !important;
        border-radius: 10px !important;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1) !important;
        margin-bottom: 20px !important;
        border: 1px solid #e0e0e0 !important;
      }

      #cashierDeliveryTab .filter-grid {
        display: grid !important;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)) !important;
        gap: 15px !important;
        margin-top: 15px !important;
      }

      #cashierDeliveryTab .filter-section {
        display: flex !important;
        flex-direction: column !important;
        gap: 8px !important;
      }

      #cashierDeliveryTab .filter-section label {
        font-weight: bold !important;
        color: var(--secondary-color) !important;
        font-size: 14px !important;
      }

      #cashierDeliveryTab .filter-section select,
      #cashierDeliveryTab .filter-section input {
        padding: 10px !important;
        border: 1px solid var(--border-color) !important;
        border-radius: 8px !important;
        font-size: 14px !important;
        width: 100% !important;
      }

      /* ==================== تحسينات جدول الدليفري في الكاشير ==================== */
      #cashierDeliveryTab .delivery-orders-container {
        background: white;
        border-radius: 12px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        padding: 20px;
        margin-top: 10px;
      }

      #cashierDeliveryTab .products-table {
        width: 100%;
        border-collapse: separate;
        border-spacing: 0 8px;
        margin-top: 5px;
      }

      #cashierDeliveryTab .products-table thead tr {
        background: linear-gradient(135deg, var(--secondary-color), #ff8a5c);
        border-radius: 10px 10px 0 0;
      }

      #cashierDeliveryTab .products-table th {
        color: white;
        font-weight: 600;
        font-size: 13px;
        padding: 12px 8px;
        text-align: center;
        border: none;
        white-space: nowrap;
      }

      #cashierDeliveryTab .products-table th:first-child {
        border-radius: 8px 0 0 8px;
      }

      #cashierDeliveryTab .products-table th:last-child {
        border-radius: 0 8px 8px 0;
      }

      #cashierDeliveryTab .products-table tbody tr {
        background: #ffffff;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
        transition: all 0.2s ease;
        border-radius: 10px;
      }

      #cashierDeliveryTab .products-table tbody tr:hover {
        transform: translateY(-2px);
        box-shadow: 0 6px 15px rgba(255, 107, 53, 0.15);
        background: #fff9f5;
      }

      #cashierDeliveryTab .products-table td {
        padding: 12px 8px;
        border: none;
        text-align: center;
        vertical-align: middle;
        background: inherit;
        font-size: 13px;
      }

      #cashierDeliveryTab .products-table td:first-child {
        border-radius: 10px 0 0 10px;
      }

      #cashierDeliveryTab .products-table td:last-child {
        border-radius: 0 10px 10px 0;
      }

      /* تنسيق حقول الإدخال داخل الجدول */
      #cashierDeliveryTab .products-table input[type="text"],
      #cashierDeliveryTab .products-table select {
        width: 100%;
        min-width: 90px;
        padding: 8px 10px;
        border: 1px solid #e0e0e0;
        border-radius: 20px;
        font-size: 12px;
        font-weight: 500;
        background: white;
        transition: all 0.2s;
        text-align: center;
        box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.05);
      }

      #cashierDeliveryTab .products-table input[type="text"]:focus,
      #cashierDeliveryTab .products-table select:focus {
        outline: none;
        border-color: var(--secondary-color);
        box-shadow: 0 0 0 3px rgba(255, 107, 53, 0.2);
      }

      #cashierDeliveryTab .products-table input[type="text"]:hover,
      #cashierDeliveryTab .products-table select:hover {
        border-color: var(--primary-color);
      }

      /* تلوين حالات الطلب في القائمة المنسدلة */
      #cashierDeliveryTab .products-table select option[value="pending"] {
        background: #fff3cd;
        color: #856404;
      }
      #cashierDeliveryTab .products-table select option[value="delivering"] {
        background: #cce5ff;
        color: #004085;
      }
      #cashierDeliveryTab .products-table select option[value="delivered"] {
        background: #d4edda;
        color: #155724;
      }
      #cashierDeliveryTab .products-table select option[value="cancelled"] {
        background: #f8d7da;
        color: #721c24;
      }

      /* عرض القيمة المحددة بلون */
      #cashierDeliveryTab .products-table select[data-status="pending"] {
        background: #fff3cd;
        color: #856404;
      }
      #cashierDeliveryTab .products-table select[data-status="delivering"] {
        background: #cce5ff;
        color: #004085;
      }
      #cashierDeliveryTab .products-table select[data-status="delivered"] {
        background: #d4edda;
        color: #155724;
      }
      #cashierDeliveryTab .products-table select[data-status="cancelled"] {
        background: #f8d7da;
        color: #721c24;
      }

      /* تنسيق خاص لخلية الإجمالي */
      #cashierDeliveryTab .products-table td:nth-last-child(2) {
        font-weight: 700;
        color: var(--secondary-color);
        background: rgba(255, 107, 53, 0.05);
        border-radius: 20px;
        font-size: 14px;
      }

      /* تنسيق أزرار الإجراءات */
      #cashierDeliveryTab .products-table .action-buttons {
        display: flex;
        gap: 6px;
        justify-content: center;
        flex-wrap: wrap;
      }

      #cashierDeliveryTab .products-table button {
        padding: 6px 10px;
        border: none;
        border-radius: 20px;
        font-size: 12px;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.2s;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 4px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      }

      #cashierDeliveryTab .products-table button i {
        font-size: 12px;
      }

      #cashierDeliveryTab .products-table button:hover {
        transform: scale(1.05);
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
      }

      /* ألوان الأزرار */
      #cashierDeliveryTab .products-table button[title="حفظ"] {
        background: #4caf50;
        color: white;
      }

      #cashierDeliveryTab .products-table button[title="تم التوصيل"] {
        background: #2196f3;
        color: white;
      }

      #cashierDeliveryTab .products-table button[title="طباعة"] {
        background: #607d8b;
        color: white;
      }

      /* تنسيق خلية رقم التوصيل */
      #cashierDeliveryTab .products-table td:nth-child(3) {
        font-weight: 600;
        color: #0d47a1;
        background: rgba(33, 150, 243, 0.1);
        border-radius: 20px;
      }

      /* تنسيق خلية العميل/المنطقة */
      #cashierDeliveryTab .products-table td:nth-child(7) {
        font-weight: 500;
        color: #2c3e50;
        max-width: 150px;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }

      /* شريط التمرير الأفقي للجدول */
      #cashierDeliveryTab .delivery-orders-container > div {
        border-radius: 10px;
      }

      /* تحسين عرض الفلترة */
      #cashierDeliveryTab .cashier-report-filter {
        background: white;
        border-radius: 12px;
        padding: 20px;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
        margin-bottom: 20px;
        border: 1px solid #f0f0f0;
      }

      #cashierDeliveryTab .filter-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
        gap: 15px;
        margin-top: 15px;
      }

      #cashierDeliveryTab .filter-section label {
        font-weight: 600;
        color: var(--secondary-color);
        font-size: 13px;
        margin-bottom: 5px;
        display: block;
      }

      #cashierDeliveryTab .filter-section input,
      #cashierDeliveryTab .filter-section select {
        width: 100%;
        padding: 10px 12px;
        border: 1px solid #e0e0e0;
        border-radius: 25px;
        font-size: 13px;
        background: white;
        transition: all 0.2s;
      }

      #cashierDeliveryTab .filter-section input:focus,
      #cashierDeliveryTab .filter-section select:focus {
        border-color: var(--secondary-color);
        box-shadow: 0 0 0 3px rgba(255, 107, 53, 0.1);
        outline: none;
      }

      /* تحسين إحصائيات الدليفري */
      #cashierDeliveryTab .delivery-stats {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 15px;
        margin-bottom: 20px;
      }

      #cashierDeliveryTab .delivery-stat-card {
        background: white;
        padding: 20px 15px;
        border-radius: 15px;
        box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
        text-align: center;
        border: 1px solid #f5f5f5;
        transition: transform 0.2s;
      }

      #cashierDeliveryTab .delivery-stat-card:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 20px rgba(255, 107, 53, 0.15);
      }

      #cashierDeliveryTab .delivery-stat-card h3 {
        color: #666;
        font-size: 13px;
        margin-bottom: 10px;
        font-weight: 600;
      }

      #cashierDeliveryTab .delivery-stat-amount {
        font-size: 24px;
        font-weight: 700;
        color: var(--secondary-color);
        line-height: 1.2;
      }

      /* تنسيق خاص للشاشات الصغيرة */
      @media (max-width: 768px) {
        #cashierDeliveryTab .products-table th,
        #cashierDeliveryTab .products-table td {
          font-size: 11px;
          padding: 8px 4px;
        }

        #cashierDeliveryTab .products-table input[type="text"],
        #cashierDeliveryTab .products-table select {
          min-width: 70px;
          padding: 6px;
          font-size: 11px;
        }

        #cashierDeliveryTab .products-table button {
          padding: 4px 6px;
          font-size: 11px;
        }
      }

      /* ==================== إصلاح شاشة المدير ==================== */
      #adminScreen .tabs {
        position: relative !important;
        z-index: 1000 !important;
        display: flex !important;
        flex-wrap: wrap !important;
        gap: 10px !important;
        margin-bottom: 20px !important;
        background: white !important;
        padding: 10px !important;
        border-radius: 10px !important;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1) !important;
      }

      #adminScreen .tab-content {
        position: relative !important;
        z-index: 1 !important;
        display: none !important;
        width: 100% !important;
        background: white !important;
        padding: 20px !important;
        border-radius: 10px !important;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1) !important;
        margin-top: 10px !important;
      }

      #adminScreen .tab-content.active {
        display: block !important;
      }

      /* ==================== تنسيقات متجاوبة إضافية ==================== */
      @media (max-width: 768px) {
        #cashierDeliveryTab .delivery-stats {
          grid-template-columns: 1fr !important;
        }

        #cashierDeliveryTab .customer-info-grid {
          grid-template-columns: 1fr !important;
        }

        #cashierDeliveryTab .delivery-fields {
          grid-template-columns: 1fr !important;
        }

        #cashierDeliveryTab .action-buttons {
          flex-direction: column !important;
        }

        #cashierDeliveryTab .action-btn {
          width: 100% !important;
        }
      }
    </style>
  </head>
  <body>
    <!-- العلامة المائية -->
    <div class="watermark">amaryasser408@gmail.com</div>

    <!-- شاشة تسجيل الدخول -->
    <div id="loginScreen" class="login-container">
      <div class="login-box">
        <img
          src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1"
          alt="كفتة على الفحم"
          class="restaurant-logo"
        />
        <h1>🍖 كفتة على الفحم</h1>
        <p style="margin-bottom: 20px; color: #666">إدارة محــمد هــاشم</p>

        <div class="role-selector">
          <button class="role-btn active" onclick="setRole('cashier')">
            <i class="fas fa-cash-register"></i>
            كاشير
          </button>
          <button class="role-btn" onclick="setRole('admin')">
            <i class="fas fa-user-shield"></i>
            مدير
          </button>
        </div>

        <div class="form-group">
          <label>اسم المستخدم</label>
          <input type="text" id="username" placeholder="أدخل اسم المستخدم" />
        </div>

        <!-- في شاشة تسجيل الدخول - قسم كلمة المرور -->
        <div class="form-group">
          <label>كلمة المرور</label>
          <div style="position: relative; display: flex; align-items: center">
            <input
              type="password"
              id="password"
              placeholder="أدخل كلمة المرور"
              style="flex: 1; padding-left: 40px"
            />
            <i
              class="fas fa-eye"
              id="togglePassword"
              style="
                position: absolute;
                left: 10px;
                cursor: pointer;
                color: #666;
              "
              onclick="togglePasswordVisibility()"
            ></i>
          </div>
        </div>

        <button class="btn btn-primary" onclick="login()">
          <i class="fas fa-sign-in-alt"></i>
          تسجيل الدخول
        </button>

        <p style="margin-top: 20px; color: #666; font-size: 12px">
          Developer Ammar Konna
        </p>
        <p style="margin-top: 5px; color: #666; font-size: 12px">
          Gmail: Amaryasser408@gmail.com
        </p>
      </div>
    </div>

    <!-- شاشة الكاشير -->
    <div id="cashierScreen" class="container">
      <div class="header">
        <div class="header-content">
          <img
            src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1"
            alt="كفتة على الفحم"
            class="header-logo"
          />
          <h1>🍖 كفتة على الفحم - نظام الكاشير</h1>
        </div>
        <div class="header-info">
          <div class="connection-status">
            <div class="connection-dot" id="connectionDot"></div>
            <span class="connection-text" id="connectionText"
              >جاري التحقق من الاتصال...</span
            >
          </div>
          <div class="save-indicator">
            <div class="save-dot"></div>
            <span>حفظ تلقائي</span>
          </div>
          <span id="cashierTime"></span>
          <span id="cashierName"></span>
          <button class="logout-btn" onclick="openExpenseModal()">
            <i class="fas fa-money-bill-wave"></i>
            صرف مصاريف
          </button>
          <button class="logout-btn" onclick="printEndOfShiftReport()">
            <i class="fas fa-file-alt"></i>
            تقرير نهاية الدوام
          </button>
          <button class="logout-btn" onclick="logout()">
            <i class="fas fa-sign-out-alt"></i>
            تسجيل الخروج
          </button>
        </div>
      </div>

      <!-- تبويبات الكاشير -->
      <div class="tabs">
        <button class="tab-btn active" onclick="switchCashierTab('pos')">
          <i class="fas fa-shopping-cart"></i> نقطة البيع
        </button>
        <button class="tab-btn" onclick="switchCashierTab('reports')">
          <i class="fas fa-chart-bar"></i> التقارير
        </button>
        <button class="tab-btn" onclick="switchCashierTab('delivery')">
          <i class="fas fa-motorcycle"></i> الدليفري
          <span
            id="pendingDeliveryCount"
            style="
              background: red;
              color: white;
              border-radius: 50%;
              padding: 2px 6px;
              font-size: 10px;
              margin-right: 5px;
              display: none;
            "
            >0</span
          >
        </button>
      </div>

      <!-- تبويب نقطة البيع -->
      <div id="cashierPosTab" class="tab-content active">
        <!-- قسم الفواتير المعلقة -->
        <div class="hold-invoices-section" id="holdInvoicesSection">
          <div class="hold-invoices-header">
            <h3>
              <i class="fas fa-pause-circle"></i>
              الفواتير المعلقة
              <span class="hold-invoices-count" id="holdInvoicesCount">0</span>
            </h3>
            <button class="btn btn-secondary" onclick="toggleHoldInvoices()">
              <i class="fas fa-chevron-down" id="holdInvoicesToggleIcon"></i>
              إخفاء
            </button>
          </div>
          <div class="hold-invoices-container" id="holdInvoicesContainer">
            <div class="empty-hold-invoices">لا توجد فواتير معلقة حالياً</div>
          </div>
        </div>

        <!-- شريط البحث -->
        <div class="search-container">
          <div class="search-icon">
            <i class="fas fa-search"></i>
          </div>
          <input
            type="text"
            id="productSearch"
            class="search-input"
            placeholder="ابحث عن منتج بالاسم..."
            oninput="searchProducts()"
          />
        </div>

        <div class="cashier-container">
          <div>
            <div style="margin-bottom: 15px">
              <button
                class="btn btn-secondary"
                onclick="displayProducts('all')"
                style="margin-left: 10px"
              >
                <i class="fas fa-th"></i>
                جميع المنتجات
              </button>
              <!-- سيتم إضافة الأقسام ديناميكياً -->
              <div id="categoryButtons" style="display: inline"></div>
            </div>
            <div id="productsContainer" class="products-grid"></div>
          </div>

          <div class="invoice-panel">
            <!-- نوع الطلب -->
            <div class="order-type-container">
              <h3>نوع الطلب:</h3>
              <div class="order-type-buttons">
                <button
                  class="order-type-btn hall active"
                  onclick="setOrderType('hall')"
                >
                  <i class="fas fa-store"></i>
                  صالة
                </button>
                <button
                  class="order-type-btn takeout"
                  onclick="setOrderType('takeout')"
                >
                  <i class="fas fa-shopping-bag"></i>
                  تيك أوت
                </button>
                <button
                  class="order-type-btn delivery"
                  onclick="setOrderType('delivery')"
                >
                  <i class="fas fa-motorcycle"></i>
                  توصيل
                </button>
              </div>
            </div>

            <!-- خيارات الفاتورة -->
            <div class="invoice-options">
              <div class="invoice-options-grid">
                <div class="invoice-option">
                  <label>رقم الطاولة (اختياري)</label>
                  <input
                    type="text"
                    id="tableNumber"
                    placeholder="أدخل رقم الطاولة"
                  />
                </div>
                <div class="invoice-option">
                  <label>رقم التوصيل</label>
                  <input
                    type="text"
                    id="deliveryNumber"
                    placeholder="أدخل رقم التوصيل"
                    oninput="checkDeliveryNumber()"
                  />
                </div>
                <div class="invoice-option">
                  <label>اسم العميل</label>
                  <input
                    type="text"
                    id="customerName"
                    placeholder="أدخل اسم العميل"
                  />
                </div>
              </div>
            </div>

            <!-- اختيار مكان التوصيل (يظهر فقط عند اختيار توصيل) -->
            <div class="delivery-location-section" id="deliveryLocationSection">
              <div class="invoice-option">
                <label>مكان التوصيل</label>
                <input
                  type="text"
                  id="deliveryLocation"
                  class="delivery-location-input"
                  placeholder="أدخل مكان التوصيل"
                />
              </div>
              <!-- منطقة اختيار منطقة التوصيل (جديد) -->
              <div id="deliveryZonesContainer" style="display: none">
                <label>اختر منطقة التوصيل:</label>
                <div
                  class="delivery-zone-buttons"
                  id="deliveryZoneButtons"
                ></div>
              </div>
            </div>

            <div class="invoice-items" id="invoiceItems">
              <div class="empty-state">
                <div class="empty-state-icon">
                  <i class="fas fa-shopping-cart"></i>
                </div>
                <p>لم تضف أي منتجات بعد</p>
              </div>
            </div>

            <!-- الخصم -->
            <div class="invoice-discount">
              <label>خصم:</label>
              <div class="invoice-discount-type">
                <div
                  class="discount-type-btn active"
                  onclick="setDiscountType('percentage')"
                >
                  %
                </div>
                <div
                  class="discount-type-btn"
                  onclick="setDiscountType('fixed')"
                >
                  جنيه
                </div>
              </div>
              <input
                type="number"
                id="discountValue"
                placeholder="0"
                min="0"
                max="100"
                onchange="updateInvoiceTotal()"
              />
            </div>

            <div class="invoice-total">
              <div class="invoice-total-label">الإجمالي:</div>
              <div class="invoice-total-amount" id="totalAmount">0.00</div>
            </div>

            <!-- ملاحظات الطلب -->
            <div class="invoice-notes">
              <label>ملاحظات الطلب</label>
              <textarea
                id="orderNotes"
                placeholder="أي ملاحظات إضافية للطلب..."
              ></textarea>
            </div>

            <div class="payment-methods">
              <button
                class="payment-btn active"
                onclick="selectPayment('cash')"
              >
                <i class="fas fa-money-bill"></i>
                كاش
              </button>
              <button class="payment-btn" onclick="selectPayment('bank')">
                <i class="fas fa-university"></i>
                بنكك
              </button>
              <button class="payment-btn" onclick="selectPayment('foori')">
                <i class="fas fa-mobile-alt"></i>
                فوري
              </button>
              <button class="payment-btn" onclick="selectPayment('okash')">
                <i class="fas fa-credit-card"></i>
                أوكاش
              </button>
              <button class="payment-btn" onclick="selectPayment('sahel')">
                <i class="fas fa-mobile-alt"></i>
                ساهل
              </button>
            </div>
            <div class="invoice-actions">
              <button class="btn btn-hold" onclick="holdInvoice()">
                <i class="fas fa-pause-circle"></i>
                تعليق الفاتورة
              </button>
              <button class="btn btn-success" onclick="completeSale()">
                <i class="fas fa-check-circle"></i>
                إتمام البيع
              </button>
              <button class="btn btn-danger" onclick="clearInvoice()">
                <i class="fas fa-trash"></i>
                مسح
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- تبويب التقارير في الكاشير -->
      <div id="cashierReportsTab" class="tab-content">
        <div class="cashier-report-filter">
          <h3 style="color: var(--secondary-color); margin-bottom: 15px">
            <i class="fas fa-filter"></i>
            فلترة التقرير اليومي
          </h3>
          <div class="filter-grid">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input type="date" id="cashierFilterStartDate" />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input type="date" id="cashierFilterEndDate" />
            </div>
            <div class="filter-section">
              <label>طريقة الدفع:</label>
              <select id="cashierFilterPayment">
                <option value="all">جميع طرق الدفع</option>
                <option value="cash">كاش</option>
                <option value="bank">بنكك</option>
                <option value="foori">فوري</option>
                <option value="okash">أوكاش</option>
                <option value="sahel">ساهل</option>
              </select>
            </div>
            <div class="filter-section">
              <label>نوع الطلب:</label>
              <select id="cashierFilterOrderType">
                <option value="all">جميع الأنواع</option>
                <option value="hall">صالة</option>
                <option value="takeout">تيك أوت</option>
                <option value="delivery">توصيل</option>
              </select>
            </div>
            <div class="filter-section">
              <label>القسم:</label>
              <select id="cashierFilterCategory">
                <option value="all">جميع الأقسام</option>
                <!-- سيتم إضافة الأقسام ديناميكياً -->
              </select>
            </div>
            <div class="filter-section" style="grid-column: span 2">
              <button
                class="btn btn-primary"
                onclick="loadCashierReport()"
                style="margin-top: 25px"
              >
                <i class="fas fa-search"></i>
                تطبيق الفلترة
              </button>
              <button class="export-btn" onclick="exportCashierReportToExcel()">
                <i class="fas fa-file-excel"></i>
                تصدير إلى Excel
              </button>
            </div>
          </div>
        </div>

        <!-- نتائج التقرير -->
        <div class="report-summary">
          <div class="summary-card">
            <h4>إجمالي المبيعات</h4>
            <div class="summary-value sales-amount" id="cashierReportTotal">
              0.00 جنيه
            </div>
          </div>
          <div class="summary-card">
            <h4>عدد الفواتير</h4>
            <div class="summary-value" id="cashierReportCount">0</div>
          </div>
          <div class="summary-card">
            <h4>متوسط قيمة الفاتورة</h4>
            <div class="summary-value" id="cashierReportAverage">0.00 جنيه</div>
          </div>
          <div class="summary-card">
            <h4>المصاريف</h4>
            <div
              class="summary-value expenses-amount"
              id="cashierReportExpenses"
            >
              0.00 جنيه
            </div>
          </div>
          <div class="summary-card">
            <h4>صافي الدخل</h4>
            <div class="summary-value net-amount" id="cashierReportNet">
              0.00 جنيه
            </div>
          </div>
        </div>

        <!-- جدول الفواتير التفصيلي -->
        <div class="panel">
          <div class="panel-header-tools">
            <h3><i class="fas fa-table"></i> تفاصيل الفواتير</h3>
            <div>
              <button class="btn btn-print" onclick="printCashierReport()">
                <i class="fas fa-print"></i> طباعة الكل
              </button>
              <button class="export-btn" onclick="exportCashierReportToExcel()">
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>

          <table class="products-table">
            <thead>
              <tr>
                <th>رقم الفاتورة</th>
                <th>التاريخ</th>
                <th>الوقت</th>
                <th>نوع الطلب</th>
                <th>طريقة الدفع</th>
                <th>عدد المنتجات</th>
                <th>الإجمالي</th>
                <th>طباعة</th>
              </tr>
            </thead>
            <tbody id="cashierReportTableBody">
              <tr>
                <td colspan="8" style="text-align: center">لا توجد بيانات</td>
              </tr>
            </tbody>
          </table>
        </div>

        <!-- جدول المنتجات الأكثر مبيعاً -->
        <div class="panel">
          <div class="panel-header-tools">
            <h3><i class="fas fa-trophy"></i> المنتجات الأكثر مبيعاً</h3>
            <div>
              <button class="btn btn-print" onclick="printTopProductsReport()">
                <i class="fas fa-print"></i> طباعة
              </button>
              <button class="export-btn" onclick="exportTopProductsToExcel()">
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>
          <table class="products-table">
            <thead>
              <tr>
                <th>#</th>
                <th>اسم المنتج</th>
                <th>عدد مرات البيع</th>
                <th>إجمالي الكمية</th>
                <th>إجمالي المبيعات</th>
              </tr>
            </thead>
            <tbody id="cashierTopProductsBody">
              <tr>
                <td colspan="5" style="text-align: center">لا توجد بيانات</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ==================== تبويب الدليفري للكاشير ==================== -->
      <div id="cashierDeliveryTab" class="tab-content">
        <!-- إحصائيات سريعة -->
        <div class="delivery-stats">
          <div class="delivery-stat-card">
            <h3>طلبات التوصيل اليوم</h3>
            <div class="delivery-stat-amount" id="todayDeliveryCount">0</div>
          </div>
          <div class="delivery-stat-card">
            <h3>قيد التوصيل</h3>
            <div class="delivery-stat-amount" id="pendingDeliveryCountStat">
              0
            </div>
          </div>
          <div class="delivery-stat-card">
            <h3>تم التوصيل</h3>
            <div class="delivery-stat-amount" id="deliveredCountStat">0</div>
          </div>
          <div class="delivery-stat-card">
            <h3>إجمالي مبيعات التوصيل</h3>
            <div class="delivery-stat-amount" id="todayDeliverySales">
              0.00 جنيه
            </div>
          </div>
        </div>

        <!-- فلترة الطلبات -->
        <div class="cashier-report-filter">
          <h3 style="color: var(--secondary-color); margin-bottom: 15px">
            <i class="fas fa-filter"></i>
            فلترة طلبات التوصيل
          </h3>
          <div class="filter-grid">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input
                type="date"
                id="userDeliveryStartDate"
                class="form-control"
              />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input
                type="date"
                id="userDeliveryEndDate"
                class="form-control"
              />
            </div>
            <div class="filter-section">
              <label>حالة الطلب:</label>
              <select id="userDeliveryStatus" class="form-control">
                <option value="all">جميع الحالات</option>
                <option value="pending">في انتظار التوصيل</option>
                <option value="delivering">قيد التوصيل</option>
                <option value="delivered">تم التوصيل</option>
                <option value="cancelled">ملغي</option>
              </select>
            </div>
            <div class="filter-section">
              <label>الموصل:</label>
              <select id="userDeliveryPersonnel" class="form-control">
                <option value="all">جميع الموصلين</option>
                <!-- سيتم تعبئتها ديناميكياً -->
              </select>
            </div>
            <div class="filter-section" style="grid-column: span 2">
              <button
                class="btn btn-primary"
                onclick="loadUserDeliveryOrders()"
              >
                <i class="fas fa-search"></i>
                تطبيق الفلترة
              </button>
              <button
                class="btn btn-excel"
                onclick="exportUserDeliveryToExcel()"
              >
                <i class="fas fa-file-excel"></i>
                تصدير Excel
              </button>
              <button class="btn btn-print" onclick="printAllDeliveryOrders()">
                <i class="fas fa-print"></i>
                طباعة الكل
              </button>
            </div>
          </div>
        </div>

        <!-- قائمة طلبات التوصيل -->
        <div class="delivery-orders-container">
          <div
            style="
              display: flex;
              justify-content: space-between;
              align-items: center;
              margin-bottom: 15px;
            "
          >
            <h3><i class="fas fa-list"></i> طلبات التوصيل</h3>
          </div>
          <div id="userDeliveryOrdersList" class="delivery-orders-list">
            <!-- سيتم تعبئتها ديناميكياً -->
            <div class="empty-state">
              <div class="empty-state-icon">
                <i class="fas fa-motorcycle"></i>
              </div>
              <p>لا توجد طلبات توصيل</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- شاشة المدير -->
    <div id="adminScreen" class="container">
      <div class="header">
        <div class="header-content">
          <img
            src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1"
            alt="كفتة على الفحم"
            class="header-logo"
          />
          <h1>🍖 كفتة على الفحم - لوحة التحكم</h1>
        </div>
        <div class="header-info">
          <div class="connection-status">
            <div class="connection-dot" id="connectionDotAdmin"></div>
            <span class="connection-text" id="connectionTextAdmin"
              >جاري التحقق من الاتصال...</span
            >
          </div>
          <div class="save-indicator">
            <div class="save-dot"></div>
            <span>حفظ تلقائي</span>
          </div>
          <!-- أضف هذا الزر في شاشة المدير داخل قسم header-info -->
          <button
            class="logout-btn"
            onclick="openReturnModal()"
            style="background: #f44336; padding: 8px 12px; font-size: 13px"
          >
            <i class="fas fa-undo-alt"></i>
            إرجاع
          </button>
          <button
            class="logout-btn"
            onclick="loadReturnsReport()"
            style="background: #9c27b0; padding: 8px 12px; font-size: 13px"
          >
            <i class="fas fa-chart-bar"></i>
            المرتجعات
          </button>
          <span id="adminTime"></span>
          <span id="adminName"></span>
          <button class="logout-btn" onclick="logout()">
            <i class="fas fa-sign-out-alt"></i>
            تسجيل الخروج
          </button>
        </div>
      </div>

      <!-- تبويبات المدير - تأكد من أن كل زر له onclick صحيح -->
      <div class="tabs">
        <button
          class="tab-btn active"
          onclick="switchAdminTab('dashboard', event)"
        >
          <i class="fas fa-tachometer-alt"></i> لوحة التحكم
        </button>
        <button class="tab-btn" onclick="switchAdminTab('products', event)">
          <i class="fas fa-box"></i> المنتجات
        </button>
        <button class="tab-btn" onclick="switchAdminTab('productSales', event)">
          <i class="fas fa-chart-line"></i> مبيعات المنتجات
        </button>
        <button class="tab-btn" onclick="switchAdminTab('sales', event)">
          <i class="fas fa-chart-line"></i> المبيعات
        </button>
        <!-- ✅ الدليفري هنا -->
        <button class="tab-btn" onclick="switchAdminTab('delivery', event)">
          <i class="fas fa-truck"></i> إدارة الدليفري
        </button>
        <button class="tab-btn" onclick="switchAdminTab('expenses', event)">
          <i class="fas fa-money-bill-wave"></i> المصاريف
        </button>
        <button class="tab-btn" onclick="switchAdminTab('categories', event)">
          <i class="fas fa-tags"></i> الأقسام
        </button>
        <button class="tab-btn" onclick="switchAdminTab('employees', event)">
          <i class="fas fa-users"></i> الموظفين
        </button>
        <button class="tab-btn" onclick="switchAdminTab('users', event)">
          <i class="fas fa-user-cog"></i> المستخدمون
        </button>
        <button
          class="tab-btn"
          onclick="switchAdminTab('restaurantInfo', event)"
        >
          <i class="fas fa-info-circle"></i> معلومات المطعم
        </button>
      </div>

      <!-- تبويب لوحة التحكم -->
      <div id="dashboardTab" class="tab-content active">
        <div class="dashboard-grid">
          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon sales">
                <i class="fas fa-money-bill-wave"></i>
              </div>
              <div class="dashboard-card-title">إجمالي المبيعات</div>
            </div>
            <div class="dashboard-card-value" id="dashboardTotalSales">
              0.00 جنيه
            </div>
            <div class="dashboard-card-change positive">
              <i class="fas fa-arrow-up"></i> 12% مقارنة بالأمس
            </div>
          </div>

          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon orders">
                <i class="fas fa-clipboard-list"></i>
              </div>
              <div class="dashboard-card-title">عدد الطلبات</div>
            </div>
            <div class="dashboard-card-value" id="dashboardTotalOrders">0</div>
            <div class="dashboard-card-change positive">
              <i class="fas fa-arrow-up"></i> 8% مقارنة بالأمس
            </div>
          </div>

          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon products">
                <i class="fas fa-box"></i>
              </div>
              <div class="dashboard-card-title">المنتجات</div>
            </div>
            <div class="dashboard-card-value" id="dashboardTotalProducts">
              0
            </div>
            <div class="dashboard-card-change">
              <i class="fas fa-minus"></i> لم يتغير
            </div>
          </div>

          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon expenses">
                <i class="fas fa-money-bill-wave"></i>
              </div>
              <div class="dashboard-card-title">المصاريف</div>
            </div>
            <div class="dashboard-card-value" id="dashboardTotalExpenses">
              0.00 جنيه
            </div>
            <div class="dashboard-card-change negative">
              <i class="fas fa-arrow-up"></i> 5% مقارنة بالأمس
            </div>
          </div>
        </div>
      </div>

      <!-- تبويب المنتجات -->
      <div id="productsTab" class="tab-content">
        <div
          class="panel-header-tools"
          style="
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
          "
        >
          <h2><i class="fas fa-box"></i> قائمة المنتجات</h2>
          <div>
            <button class="btn btn-print" onclick="printProducts()">
              <i class="fas fa-print"></i> طباعة
            </button>
            <button class="btn btn-excel" onclick="exportProductsToExcel()">
              <i class="fas fa-file-excel"></i> Excel
            </button>
          </div>
        </div>
        <div class="admin-container">
          <div class="panel">
            <h2>
              <i class="fas fa-plus-circle"></i>
              إضافة منتج جديد
            </h2>
            <div class="form-group">
              <label>اسم المنتج</label>
              <input
                type="text"
                id="productName"
                placeholder="مثال: كفتة مشوية"
              />
            </div>
            <div class="form-group">
              <label>السعر</label>
              <input type="number" id="productPrice" placeholder="0.00" />
            </div>
            <div class="form-group">
              <label>القسم</label>
              <select id="productCategory">
                <!-- سيتم إضافة الأقسام ديناميكياً -->
              </select>
            </div>
            <div class="form-group">
              <label>رابط الصورة</label>
              <input
                type="text"
                id="productImage"
                placeholder="https://example.com/image.jpg"
              />
            </div>

            <!-- قسم المكونات اليدوية -->
            <div class="product-ingredients-manual">
              <div class="product-ingredients-manual-header">
                <h3><i class="fas fa-carrot"></i> مكونات المنتج (يدوي)</h3>
              </div>
              <div
                class="product-ingredients-manual-list"
                id="productIngredientsManualList"
              >
                <div class="empty-state">
                  <div class="empty-state-icon">
                    <i class="fas fa-carrot"></i>
                  </div>
                  <p>لم تضف أي مكونات بعد</p>
                </div>
              </div>
              <div class="add-product-ingredient-manual-form">
                <input
                  type="text"
                  id="manualIngredientName"
                  placeholder="اسم المكون"
                />
                <input
                  type="text"
                  id="manualIngredientQuantity"
                  placeholder="الكمية"
                />
                <select
                  id="manualIngredientUnit"
                  class="ingredient-unit-select"
                >
                  <option value="قطعة">قطعة</option>
                  <option value="جرام">جرام</option>
                  <option value="كيلو">كيلو</option>
                  <option value="مل">مل</option>
                  <option value="لتر">لتر</option>
                </select>
                <button
                  class="btn btn-secondary"
                  onclick="addManualIngredient()"
                >
                  <i class="fas fa-plus"></i>
                  إضافة
                </button>
              </div>
            </div>

            <button class="btn btn-success" onclick="addProduct()">
              <i class="fas fa-save"></i>
              إضافة المنتج
            </button>
          </div>

          <div class="panel">
            <table class="products-table">
              <thead>
                <tr>
                  <th>الصورة</th>
                  <th>الاسم</th>
                  <th>السعر</th>
                  <th>القسم</th>
                  <th>المكونات</th>
                  <th>الإجراءات</th>
                </tr>
              </thead>
              <tbody id="productsTableBody"></tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- تبويب مبيعات المنتجات -->
      <div id="productSalesTab" class="tab-content">
        <div class="product-sales-container">
          <div class="product-sales-header">
            <h2><i class="fas fa-chart-line"></i> مبيعات المنتجات والمكونات</h2>
            <div>
              <button class="btn btn-print" onclick="printProductSales()">
                <i class="fas fa-print"></i> طباعة
              </button>
              <button
                class="btn btn-excel"
                onclick="exportProductSalesToExcel()"
              >
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>

          <div class="product-sales-filter">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input type="date" id="productSalesStartDate" />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input type="date" id="productSalesEndDate" />
            </div>
            <div class="filter-section">
              <label>المنتج:</label>
              <select id="productSalesFilterProduct">
                <option value="all">جميع المنتجات</option>
                <!-- سيتم إضافة المنتجات ديناميكياً -->
              </select>
            </div>
            <div class="filter-section">
              <button class="btn btn-primary" onclick="loadProductSales()">
                <i class="fas fa-search"></i>
                تطبيق الفلترة
              </button>
            </div>
          </div>

          <table class="product-sales-table">
            <thead>
              <tr>
                <th>اسم المنتج</th>
                <th>عدد مرات البيع</th>
                <th>إجمالي الكمية</th>
                <th>إجمالي المبيعات</th>
                <th>المكونات المستهلكة</th>
              </tr>
            </thead>
            <tbody id="productSalesTableBody">
              <tr>
                <td colspan="5" style="text-align: center">لا توجد بيانات</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- تبويب المبيعات -->
      <div id="salesTab" class="tab-content">
        <div class="sales-filter-section">
          <div class="sales-filter-header">
            <h2><i class="fas fa-chart-line"></i> فلترة المبيعات</h2>
            <div>
              <button class="btn btn-primary" onclick="loadAdminSales()">
                <i class="fas fa-search"></i>
                تطبيق الفلترة
              </button>
              <button class="btn btn-print" onclick="printAdminSales()">
                <i class="fas fa-print"></i> طباعة
              </button>
              <button class="export-btn" onclick="exportAdminSalesToExcel()">
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>

          <div class="sales-filter-grid">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input type="date" id="salesFilterStartDate" />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input type="date" id="salesFilterEndDate" />
            </div>
            <div class="filter-section">
              <label>💰 طريقة الدفع:</label>
              <select id="salesPaymentMethod" class="form-control">
                <!-- تم تغيير المعرف من adminDeliveryPaymentMethod إلى salesPaymentMethod -->
                <option value="all">جميع طرق الدفع</option>
                <option value="cash">💵 كاش</option>
                <option value="bank">🏦 بنكك</option>
                <option value="foori">📱 فوري</option>
                <option value="okash">💳 أوكاش</option>
                <option value="sahel">📲 ساهل</option>
              </select>
            </div>
            <div class="filter-section">
              <label>المستخدم:</label>
              <select id="salesFilterUser">
                <option value="all">جميع المستخدمين</option>
                <!-- سيتم إضافة المستخدمين ديناميكياً -->
              </select>
            </div>
            <div class="filter-section">
              <label>القسم:</label>
              <select id="salesFilterCategory">
                <option value="all">جميع الأقسام</option>
                <!-- سيتم إضافة الأقسام ديناميكياً -->
              </select>
            </div>
          </div>
        </div>

        <div class="panel">
          <table id="salesTable" class="products-table">
            <thead>
              <tr>
                <th>رقم الفاتورة</th>
                <th>التاريخ</th>
                <th>الوقت</th>
                <th>المنتجات</th>
                <th>نوع الطلب</th>
                <th>عدد المنتجات</th>
                <th>الإجمالي</th>
                <th>طريقة الدفع</th>
                <th>الكاشير</th>
                <th>الإجراءات</th>
              </tr>
            </thead>
            <tbody id="salesTableBody"></tbody>
          </table>
        </div>
      </div>

      <!-- ==================== تبويب إدارة الدليفري للمدير ==================== -->
      <div id="deliveryTab" class="tab-content">
        <!-- لوحة تحكم الدليفري -->
        <div class="dashboard-grid" style="margin-bottom: 20px">
          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon orders">
                <i class="fas fa-motorcycle"></i>
              </div>
              <div class="dashboard-card-title">إجمالي طلبات التوصيل</div>
            </div>
            <div class="dashboard-card-value" id="adminTotalDeliveryOrders">
              0
            </div>
          </div>
          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon orders">
                <i class="fas fa-hourglass-half"></i>
              </div>
              <div class="dashboard-card-title">قيد التوصيل</div>
            </div>
            <div class="dashboard-card-value" id="adminPendingDelivery">0</div>
          </div>
          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon sales">
                <i class="fas fa-check-circle"></i>
              </div>
              <div class="dashboard-card-title">تم التوصيل</div>
            </div>
            <div class="dashboard-card-value" id="adminDeliveredOrders">0</div>
          </div>
          <div class="dashboard-card">
            <div class="dashboard-card-header">
              <div class="dashboard-card-icon sales">
                <i class="fas fa-money-bill-wave"></i>
              </div>
              <div class="dashboard-card-title">إجمالي مبيعات التوصيل</div>
            </div>
            <div class="dashboard-card-value" id="adminTotalDeliverySales">
              0.00 جنيه
            </div>
          </div>
        </div>

        <!-- فلترة متقدمة لتقارير الدليفري -->
        <div class="sales-filter-section">
          <div class="sales-filter-header">
            <h3><i class="fas fa-chart-line"></i> تقارير الدليفري</h3>
            <div>
              <button
                class="btn btn-primary"
                onclick="loadAdminDeliveryOrders()"
              >
                <i class="fas fa-search"></i> تطبيق الفلترة
              </button>
              <button
                class="btn btn-excel"
                onclick="exportAdminDeliveryToExcel()"
              >
                <i class="fas fa-file-excel"></i> تصدير Excel
              </button>
              <button
                class="btn btn-print"
                onclick="printAdminDeliveryReport()"
              >
                <i class="fas fa-print"></i> طباعة التقرير
              </button>
            </div>
          </div>

          <div class="filter-grid">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input
                type="date"
                id="adminDeliveryStartDate"
                class="form-control"
              />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input
                type="date"
                id="adminDeliveryEndDate"
                class="form-control"
              />
            </div>
            <div class="filter-section">
              <label>حالة الطلب:</label>
              <select id="adminDeliveryStatus" class="form-control">
                <option value="all">جميع الحالات</option>
                <option value="pending">🟡 في انتظار التوصيل</option>
                <option value="delivering">🔵 قيد التوصيل</option>
                <option value="delivered">✅ تم التوصيل</option>
                <option value="cancelled">❌ ملغي</option>
              </select>
            </div>
            <div class="filter-section">
              <label>💰 طريقة الدفع:</label>
              <select id="deliveryPaymentMethod" class="form-control">
                <!-- تم تغيير المعرف من adminDeliveryPaymentMethod إلى deliveryPaymentMethod -->
                <option value="all">جميع طرق الدفع</option>
                <option value="cash">💵 كاش</option>
                <option value="bank">🏦 بنكك</option>
                <option value="foori">📱 فوري</option>
                <option value="okash">💳 أوكاش</option>
                <option value="sahel">📲 ساهل</option>
              </select>
            </div>

            <div class="filter-section">
              <label>🚚 اسم الموصل:</label>
              <input
                type="text"
                id="adminDeliveryPersonnelName"
                class="form-control"
                placeholder="ابحث عن موصل..."
              />
            </div>
            <div class="filter-section">
              <label>الكاشير:</label>
              <select id="adminDeliveryCashier" class="form-control">
                <option value="all">جميع الكاشيرات</option>
              </select>
            </div>
          </div>
        </div>

        <!-- جدول طلبات التوصيل للمدير -->
        <div class="panel">
          <div class="panel-header-tools">
            <h3><i class="fas fa-truck"></i> جميع طلبات التوصيل</h3>
            <span
              id="adminDeliveryCount"
              style="
                background: var(--primary-color);
                padding: 5px 10px;
                border-radius: 20px;
              "
              >0</span
            >
          </div>
          <div style="overflow-x: auto">
            <table class="products-table">
              <thead>
                <tr>
                  <th>رقم الفاتورة</th>
                  <th>التاريخ</th>
                  <th>الوقت</th>
                  <th>العميل</th>
                  <th>مكان التوصيل</th>
                  <th>رقم التوصيل</th>
                  <th>🚚 الموصل</th>
                  <th>💰 طريقة الدفع</th>
                  <th>الحالة</th>
                  <th>الإجمالي</th>
                  <th>الكاشير</th>
                  <th>الإجراءات</th>
                </tr>
              </thead>
              <tbody id="adminDeliveryOrdersTableBody">
                <tr>
                  <td colspan="12" style="text-align: center">
                    لا توجد بيانات
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- تبويب المصاريف -->
      <div id="expensesTab" class="tab-content">
        <div class="expenses-filter-section">
          <div class="expenses-filter-header">
            <h2><i class="fas fa-money-bill-wave"></i> فلترة المصاريف</h2>
            <div>
              <button class="btn btn-primary" onclick="loadExpenses()">
                <i class="fas fa-search"></i>
                تطبيق الفلترة
              </button>
              <button class="btn btn-print" onclick="printExpenses()">
                <i class="fas fa-print"></i> طباعة
              </button>
              <button class="export-btn" onclick="exportExpensesToExcel()">
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>

          <div class="expenses-filter-grid">
            <div class="filter-section">
              <label>من تاريخ:</label>
              <input type="date" id="expensesFilterStartDate" />
            </div>
            <div class="filter-section">
              <label>إلى تاريخ:</label>
              <input type="date" id="expensesFilterEndDate" />
            </div>
            <div class="filter-section">
              <label>المستخدم:</label>
              <select id="expensesFilterUser">
                <option value="all">جميع المستخدمين</option>
                <!-- سيتم إضافة المستخدمين ديناميكياً -->
              </select>
            </div>
          </div>
        </div>

        <div class="admin-container">
          <div class="panel">
            <h2>
              <i class="fas fa-plus-circle"></i>
              إضافة مصروف جديد
            </h2>
            <div class="form-group">
              <label>المبلغ</label>
              <input type="number" id="expenseAmount" placeholder="0.00" />
            </div>
            <div class="form-group">
              <label>الوصف</label>
              <input
                type="text"
                id="expenseDescription"
                placeholder="وصف المصروف"
              />
            </div>
            <div class="form-group">
              <label>التاريخ</label>
              <input type="date" id="expenseDate" />
            </div>
            <button class="btn btn-success" onclick="addExpense()">
              <i class="fas fa-save"></i>
              إضافة المصروف
            </button>
          </div>

          <div class="panel">
            <table id="expensesTable" class="products-table">
              <thead>
                <tr>
                  <th>التاريخ</th>
                  <th>الوقت</th>
                  <th>الوصف</th>
                  <th>المبلغ</th>
                  <th>المستخدم</th>
                  <th>الإجراءات</th>
                </tr>
              </thead>
              <tbody id="expensesTableBody"></tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- تبويب الأقسام -->
      <div id="categoriesTab" class="tab-content">
        <div class="panel">
          <div class="panel-header-tools">
            <h2><i class="fas fa-tags"></i> إدارة الأقسام</h2>
            <div>
              <button class="btn btn-print" onclick="printCategories()">
                <i class="fas fa-print"></i> طباعة
              </button>
              <button class="btn btn-excel" onclick="exportCategoriesToExcel()">
                <i class="fas fa-file-excel"></i> Excel
              </button>
            </div>
          </div>
          <div class="categories-management">
            <h3>الأقسام الحالية:</h3>
            <div class="category-list" id="categoriesList"></div>

            <h3>إضافة قسم جديد:</h3>
            <div class="add-category-form">
              <input type="text" id="newCategoryName" placeholder="اسم القسم" />
              <button class="btn btn-success" onclick="addCategory()">
                <i class="fas fa-plus"></i>
                إضافة قسم
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- تبويب الموظفين -->
      <div id="employeesTab" class="tab-content">
        <div
          class="panel-header-tools"
          style="
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
          "
        >
          <h2><i class="fas fa-users"></i> قائمة الموظفين</h2>
          <div>
            <button class="btn btn-info" onclick="generateMonthlyReport()">
              <i class="fas fa-file-alt"></i> تقرير شهري
            </button>
            <button class="btn btn-warning" onclick="resetMonthlyData()">
              <i class="fas fa-sync-alt"></i> تصفير شهري
            </button>
            <button class="btn btn-print" onclick="printEmployeesReport()">
              <i class="fas fa-print"></i> طباعة الجميع
            </button>
            <button class="btn btn-excel" onclick="exportEmployeesToExcel()">
              <i class="fas fa-file-excel"></i> Excel
            </button>
          </div>
        </div>

        <!-- فلترة الموظفين -->
        <div class="sales-filter-section">
          <div class="sales-filter-header">
            <h2><i class="fas fa-filter"></i> فلترة تقارير الموظفين</h2>
          </div>
          <div class="sales-filter-grid">
            <div class="filter-section">
              <label>الشهر:</label>
              <select id="employeeFilterMonth">
                <option value="all">جميع الأشهر</option>
                <option value="1">يناير</option>
                <option value="2">فبراير</option>
                <option value="3">مارس</option>
                <option value="4">أبريل</option>
                <option value="5">مايو</option>
                <option value="6">يونيو</option>
                <option value="7">يوليو</option>
                <option value="8">أغسطس</option>
                <option value="9">سبتمبر</option>
                <option value="10">أكتوبر</option>
                <option value="11">نوفمبر</option>
                <option value="12">ديسمبر</option>
              </select>
            </div>
            <div class="filter-section">
              <label>السنة:</label>
              <select id="employeeFilterYear">
                <!-- سيتم تعبئتها ديناميكياً -->
              </select>
            </div>
            <div class="filter-section">
              <label>الحالة:</label>
              <select id="employeeFilterStatus">
                <option value="all">جميع الحالات</option>
                <option value="active">نشط</option>
                <option value="inactive">غير نشط</option>
              </select>
            </div>
            <div class="filter-section">
              <button class="btn btn-primary" onclick="loadFilteredEmployees()">
                <i class="fas fa-search"></i> تطبيق الفلترة
              </button>
            </div>
          </div>
        </div>

        <div class="admin-container">
          <div class="panel">
            <h2>
              <i class="fas fa-plus-circle"></i>
              إضافة موظف جديد
            </h2>
            <div class="form-group">
              <label>الاسم الكامل</label>
              <input
                type="text"
                id="employeeFullName"
                placeholder="الاسم الكامل"
              />
            </div>
            <div class="form-group">
              <label>رقم الهاتف</label>
              <input type="text" id="employeePhone" placeholder="رقم الهاتف" />
            </div>
            <div class="form-group">
              <label>الراتب الأساسي</label>
              <input type="number" id="employeeSalary" placeholder="0.00" />
            </div>
            <div class="form-group">
              <label>المسمى الوظيفي</label>
              <input
                type="text"
                id="employeePosition"
                placeholder="المسمى الوظيفي"
              />
            </div>
            <div class="form-group">
              <label>تاريخ التعيين</label>
              <input type="date" id="employeeHireDate" />
            </div>
            <button class="btn btn-success" onclick="addEmployee()">
              <i class="fas fa-save"></i>
              إضافة الموظف
            </button>
          </div>

          <div id="employeesList" class="employees-container"></div>
        </div>
      </div>

      <!-- تبويب المستخدمين -->
      <div id="usersTab" class="tab-content">
        <div
          class="panel-header-tools"
          style="
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
          "
        >
          <h2><i class="fas fa-users"></i> قائمة المستخدمين</h2>
          <div>
            <button class="btn btn-print" onclick="printUsers()">
              <i class="fas fa-print"></i> طباعة
            </button>
            <button class="btn btn-excel" onclick="exportUsersToExcel()">
              <i class="fas fa-file-excel"></i> Excel
            </button>
          </div>
        </div>
        <div class="users-container">
          <div class="panel">
            <h2>
              <i class="fas fa-plus-circle"></i>
              إضافة مستخدم جديد
            </h2>
            <div class="form-group">
              <label>اسم المستخدم</label>
              <input type="text" id="newUsername" placeholder="اسم المستخدم" />
            </div>
            <div class="form-group">
              <label>الاسم الكامل</label>
              <input type="text" id="newFullName" placeholder="الاسم الكامل" />
            </div>
            <div class="form-group">
              <label>كلمة المرور</label>
              <input
                type="password"
                id="newPassword"
                placeholder="كلمة المرور"
              />
            </div>
            <div class="form-group">
              <label>الدور</label>
              <select id="newUserRole">
                <option value="cashier">كاشير</option>
                <option value="admin">مدير</option>
              </select>
            </div>
            <button class="btn btn-success" onclick="addUser()">
              <i class="fas fa-save"></i>
              إضافة المستخدم
            </button>
          </div>

          <div id="usersList" class="users-container"></div>
        </div>
      </div>

      <!-- تبويب معلومات المطعم -->
      <div id="restaurantInfoTab" class="tab-content">
        <div class="panel">
          <div class="panel-header-tools">
            <h2><i class="fas fa-info-circle"></i> معلومات المطعم</h2>
            <div>
              <button class="btn btn-success" onclick="saveRestaurantInfo()">
                <i class="fas fa-save"></i> حفظ المعلومات
              </button>
            </div>
          </div>

          <div class="info-form">
            <div class="form-group">
              <label>اسم المطعم</label>
              <input
                type="text"
                id="restaurantName"
                placeholder="كفتة على الفحم"
              />
            </div>
            <div class="form-group">
              <label>رقم الفرع</label>
              <input
                type="text"
                id="restaurantNumber"
                placeholder="أدخل رقم الفرع"
              />
            </div>
            <div class="form-group">
              <label>اسم الفرع</label>
              <input type="text" id="branchName" placeholder="أدخل اسم الفرع" />
            </div>
          </div>

          <!-- أسعار التوصيل حسب المنطقة (جديد) -->
          <div class="delivery-prices-section">
            <h3>🚚 أسعار التوصيل حسب المنطقة</h3>
            <div class="delivery-prices-grid" id="deliveryPricesGrid">
              <div class="price-input">
                <label>منطقة 1</label>
                <input
                  type="number"
                  id="zonePrice1"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
              <div class="price-input">
                <label>منطقة 2</label>
                <input
                  type="number"
                  id="zonePrice2"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
              <div class="price-input">
                <label>منطقة 3</label>
                <input
                  type="number"
                  id="zonePrice3"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
              <div class="price-input">
                <label>منطقة 4</label>
                <input
                  type="number"
                  id="zonePrice4"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
              <div class="price-input">
                <label>منطقة 5</label>
                <input
                  type="number"
                  id="zonePrice5"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
              <div class="price-input">
                <label>منطقة 6</label>
                <input
                  type="number"
                  id="zonePrice6"
                  value="0"
                  min="0"
                  step="1"
                />
              </div>
            </div>
            <p style="font-size: 12px; color: #666; margin-top: 10px">
              حدد أسعار التوصيل لكل منطقة. سيتم عرضها للكاشير عند اختيار توصيل.
            </p>
          </div>

          <div class="delivery-numbers-management">
            <h3>أرقام التوصيل</h3>
            <div class="delivery-numbers-list" id="deliveryNumbersList"></div>

            <div class="add-delivery-number-form">
              <input
                type="text"
                id="newDeliveryNumber"
                placeholder="أدخل رقم التوصيل"
              />
              <button class="btn btn-success" onclick="addDeliveryNumber()">
                <i class="fas fa-plus"></i>
                إضافة رقم
              </button>
            </div>

            <!-- إضافة عدة أرقام دفعة واحدة -->
            <div class="add-delivery-number-form">
              <textarea
                id="multipleDeliveryNumbers"
                placeholder="أدخل أرقام التوصيل (رقم في كل سطر)"
                rows="4"
                style="
                  width: 100%;
                  padding: 10px;
                  border: 1px solid var(--border-color);
                  border-radius: 8px;
                  text-align: right;
                "
              ></textarea>
              <button
                class="btn btn-success"
                onclick="addMultipleDeliveryNumbers()"
              >
                <i class="fas fa-plus"></i>
                إضافة أرقام متعددة
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- نافذة اختيار الكمية -->
    <div
      id="quantityModal"
      class="quantity-modal-overlay"
      style="display: none"
    >
      <div class="quantity-modal">
        <div class="quantity-modal-header">
          <button class="quantity-modal-close" onclick="closeQuantityModal()">
            <i class="fas fa-times"></i>
          </button>
          <div class="quantity-modal-product" id="modalProductName">
            اسم المنتج
          </div>
          <div class="quantity-modal-price" id="modalProductPrice">
            0.00 جنيه
          </div>
        </div>

        <div class="quantity-display">
          <div class="quantity-value" id="quantityValue">1</div>
          <div class="quantity-max-notice">الحد الأقصى: 999</div>
        </div>

        <!-- أزرار الكمية السريعة -->
        <div class="quick-quantity-buttons">
          <button class="quick-quantity-btn" onclick="setQuickQuantity(1)">
            +1
          </button>
          <button class="quick-quantity-btn" onclick="setQuickQuantity(2)">
            +2
          </button>
          <button class="quick-quantity-btn" onclick="setQuickQuantity(5)">
            +5
          </button>
          <button class="quick-quantity-btn" onclick="setQuickQuantity(10)">
            +10
          </button>
        </div>

        <div class="quantity-keypad">
          <div class="quantity-buttons-grid">
            <button class="quantity-btn number" onclick="addNumber(1)">
              1
            </button>
            <button class="quantity-btn number" onclick="addNumber(2)">
              2
            </button>
            <button class="quantity-btn number" onclick="addNumber(3)">
              3
            </button>
            <button class="quantity-btn number" onclick="addNumber(4)">
              4
            </button>
            <button class="quantity-btn number" onclick="addNumber(5)">
              5
            </button>
            <button class="quantity-btn number" onclick="addNumber(6)">
              6
            </button>
            <button class="quantity-btn number" onclick="addNumber(7)">
              7
            </button>
            <button class="quantity-btn number" onclick="addNumber(8)">
              8
            </button>
            <button class="quantity-btn number" onclick="addNumber(9)">
              9
            </button>
            <button class="quantity-btn double-zero" onclick="addDoubleZero()">
              00
            </button>
            <button class="quantity-btn number" onclick="addNumber(0)">
              0
            </button>
            <button class="quantity-btn backspace" onclick="backspace()">
              <i class="fas fa-backspace"></i>
            </button>
          </div>

          <div class="quantity-action-buttons">
            <button
              class="quantity-action-btn quantity-cancel-btn"
              onclick="closeQuantityModal()"
            >
              <i class="fas fa-times"></i>
              إلغاء
            </button>
            <button
              class="quantity-action-btn quantity-add-btn"
              id="addToInvoiceBtn"
              onclick="addToInvoiceWithQuantity()"
            >
              <i class="fas fa-plus"></i>
              إضافة للفاتورة
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- نافذة صرف المصاريف -->
    <div id="expenseModal" class="quantity-modal-overlay" style="display: none">
      <div class="quantity-modal">
        <div class="quantity-modal-header">
          <button class="quantity-modal-close" onclick="closeExpenseModal()">
            <i class="fas fa-times"></i>
          </button>
          <div class="quantity-modal-product">
            <i class="fas fa-money-bill-wave"></i>
            صرف مصاريف
          </div>
          <div class="quantity-modal-price">تسجيل مبلغ مصروف</div>
        </div>

        <div class="quantity-display">
          <div class="form-group" style="margin-bottom: 20px">
            <label>المبلغ (جنيه)</label>
            <input
              type="number"
              id="expenseModalAmount"
              placeholder="0.00"
              style="
                width: 100%;
                padding: 12px;
                border: 1px solid var(--border-color);
                border-radius: 8px;
                font-size: 24px;
                text-align: center;
                direction: ltr;
              "
            />
          </div>
          <div class="form-group">
            <label>الوصف (اختياري)</label>
            <input
              type="text"
              id="expenseModalDescription"
              placeholder="سبب الصرف"
              style="
                width: 100%;
                padding: 12px;
                border: 1px solid var(--border-color);
                border-radius: 8px;
                text-align: right;
              "
            />
          </div>
        </div>

        <div class="quantity-keypad">
          <div class="quantity-action-buttons">
            <button
              class="quantity-action-btn quantity-cancel-btn"
              onclick="closeExpenseModal()"
            >
              <i class="fas fa-times"></i>
              إلغاء
            </button>
            <button
              class="quantity-action-btn quantity-add-btn"
              onclick="saveExpense()"
            >
              <i class="fas fa-save"></i>
              حفظ المصروف
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- نافذة إدارة الموظف -->
    <div
      id="employeeModal"
      class="quantity-modal-overlay"
      style="display: none"
    >
      <div class="quantity-modal">
        <div class="quantity-modal-header">
          <button class="quantity-modal-close" onclick="closeEmployeeModal()">
            <i class="fas fa-times"></i>
          </button>
          <div class="quantity-modal-product" id="employeeModalTitle">
            <i class="fas fa-user"></i>
            إدارة الموظف
          </div>
          <div class="quantity-modal-price" id="employeeModalSubtitle"></div>
        </div>

        <div
          class="quantity-display"
          style="max-height: 400px; overflow-y: auto; padding: 20px"
        >
          <div id="employeeModalContent">
            <!-- المحتوى سيتم تعبئته ديناميكياً -->
          </div>
        </div>

        <div class="quantity-keypad">
          <div class="quantity-action-buttons">
            <button
              class="quantity-action-btn quantity-cancel-btn"
              onclick="closeEmployeeModal()"
            >
              <i class="fas fa-times"></i>
              إلغاء
            </button>
            <button
              class="quantity-action-btn quantity-add-btn"
              id="saveEmployeeActionBtn"
            >
              <i class="fas fa-save"></i>
              حفظ
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- نافذة تعديل الموظف -->
    <div
      id="editEmployeeModal"
      class="quantity-modal-overlay"
      style="display: none"
    >
      <div class="quantity-modal">
        <div class="quantity-modal-header">
          <button
            class="quantity-modal-close"
            onclick="closeEditEmployeeModal()"
          >
            <i class="fas fa-times"></i>
          </button>
          <div class="quantity-modal-product">
            <i class="fas fa-user-edit"></i>
            تعديل بيانات الموظف
          </div>
        </div>

        <div
          class="quantity-display"
          style="max-height: 400px; overflow-y: auto"
        >
          <div class="form-group">
            <label>الاسم الكامل</label>
            <input
              type="text"
              id="editEmployeeFullName"
              placeholder="الاسم الكامل"
            />
          </div>
          <div class="form-group">
            <label>رقم الهاتف</label>
            <input
              type="text"
              id="editEmployeePhone"
              placeholder="رقم الهاتف"
            />
          </div>
          <div class="form-group">
            <label>الراتب الأساسي</label>
            <input type="number" id="editEmployeeSalary" placeholder="0.00" />
          </div>
          <div class="form-group">
            <label>المسمى الوظيفي</label>
            <input
              type="text"
              id="editEmployeePosition"
              placeholder="المسمى الوظيفي"
            />
          </div>
          <div class="form-group">
            <label>الحالة</label>
            <select id="editEmployeeStatus">
              <option value="active">نشط</option>
              <option value="inactive">غير نشط</option>
            </select>
          </div>
        </div>

        <div class="quantity-keypad">
          <div class="quantity-action-buttons">
            <button
              class="quantity-action-btn quantity-cancel-btn"
              onclick="closeEditEmployeeModal()"
            >
              <i class="fas fa-times"></i>
              إلغاء
            </button>
            <button
              class="quantity-action-btn quantity-add-btn"
              onclick="saveEditedEmployee()"
            >
              <i class="fas fa-save"></i>
              حفظ التعديلات
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- نافذة طباعة تقرير الموظف -->
    <div
      id="printEmployeeReportModal"
      class="quantity-modal-overlay"
      style="display: none"
    >
      <div class="quantity-modal" style="max-width: 800px">
        <div class="quantity-modal-header">
          <button
            class="quantity-modal-close"
            onclick="closePrintReportModal()"
          >
            <i class="fas fa-times"></i>
          </button>
          <div class="quantity-modal-product">
            <i class="fas fa-print"></i>
            طباعة تقرير الموظف
          </div>
        </div>

        <div
          class="quantity-display"
          style="max-height: 500px; overflow-y: auto; padding: 20px"
        >
          <div id="printReportContent">
            <!-- محتوى التقرير للطباعة -->
          </div>
        </div>

        <div class="quantity-keypad">
          <div class="quantity-action-buttons">
            <button
              class="quantity-action-btn quantity-cancel-btn"
              onclick="closePrintReportModal()"
            >
              <i class="fas fa-times"></i>
              إغلاق
            </button>
            <button
              class="quantity-action-btn quantity-add-btn"
              onclick="printEmployeeReportNow()"
            >
              <i class="fas fa-print"></i>
              طباعة التقرير
            </button>
          </div>
        </div>
      </div>
    </div>

    <script>
      // ==================== إعداد Firebase ====================
      const firebaseConfig = {
        apiKey: "AIzaSyAI8AjUMmUdIP2IIchf7XTYZ2hcCa79aQ8",
        authDomain: "kofta-b2885.firebaseapp.com",
        databaseURL: "https://kofta-b2885-default-rtdb.firebaseio.com",
        projectId: "kofta-b2885",
        storageBucket: "kofta-b2885.firebasestorage.app",
        messagingSenderId: "622180720773",
        appId: "1:622180720773:web:b75bee4745d5a5482449ec",
        measurementId: "G-W5C0ZLYP2M",
      };

      // تهيئة Firebase
      firebase.initializeApp(firebaseConfig);
      const db = firebase.firestore();
      const auth = firebase.auth();

      // ==================== مدير البيانات (DataManager) ====================
      const DataManager = {
        // المنتجات
        saveProducts: async (data) => {
          try {
            await db.collection("products").doc("all_products").set({
              data: data,
              timestamp: new Date().toISOString(),
              lastSync: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getProducts: async () => {
          try {
            const doc = await db
              .collection("products")
              .doc("all_products")
              .get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل المنتجات:", error);
            return [];
          }
        },

        // المبيعات
        saveSales: async (data) => {
          try {
            await db
              .collection("sales")
              .doc("all_sales")
              .set({
                data: data,
                lastUpdated: new Date().toISOString(),
                count: data.length,
                totalAmount: data.reduce(
                  (sum, sale) => sum + (sale.finalTotal || sale.total),
                  0,
                ),
              });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getSales: async () => {
          try {
            const doc = await db.collection("sales").doc("all_sales").get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل المبيعات:", error);
            return [];
          }
        },

        // طلبات التوصيل
        // طلبات التوصيل
        saveDeliveryOrders: async (data) => {
          try {
            await db.collection("delivery").doc("all_orders").set({
              data: data,
              lastUpdated: new Date().toISOString(),
              count: data.length,
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getDeliveryOrders: async () => {
          try {
            const doc = await db.collection("delivery").doc("all_orders").get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل طلبات التوصيل:", error);
            return [];
          }
        },

        // الموصلين (اختياري، قد تحتاجها لاحقاً)
        saveDeliveryPersonnel: async (data) => {
          try {
            await db.collection("delivery").doc("personnel").set({
              data: data,
              lastUpdated: new Date().toISOString(),
              count: data.length,
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getDeliveryPersonnel: async () => {
          try {
            const doc = await db.collection("delivery").doc("personnel").get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل الموصلين:", error);
            return [];
          }
        },

        // المصاريف
        saveExpenses: async (data) => {
          try {
            await db
              .collection("expenses")
              .doc("all_expenses")
              .set({
                data: data,
                lastUpdated: new Date().toISOString(),
                totalAmount: data.reduce(
                  (sum, expense) => sum + expense.amount,
                  0,
                ),
              });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getExpenses: async () => {
          try {
            const doc = await db
              .collection("expenses")
              .doc("all_expenses")
              .get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل المصاريف:", error);
            return [];
          }
        },

        // الطلبات
        saveOrders: async (data) => {
          try {
            await db.collection("orders").doc("all_orders").set({
              data: data,
              lastUpdated: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getOrders: async () => {
          try {
            const doc = await db.collection("orders").doc("all_orders").get();
            return doc.exists ? doc.data().data : [];
          } catch (error) {
            console.error("❌ خطأ في تحميل الطلبات:", error);
            return [];
          }
        },

        // الأقسام
        saveCategories: async (data) => {
          try {
            await db.collection("categories").doc("all_categories").set({
              data: data,
              lastUpdated: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getCategories: async () => {
          try {
            const doc = await db
              .collection("categories")
              .doc("all_categories")
              .get();
            if (doc.exists) return doc.data().data;

            const defaultCategories = [
              { id: "food", name: "مأكولات" },
              { id: "sandwiches", name: "سندوتشات" },
              { id: "drinks", name: "مشروبات" },
            ];
            return defaultCategories;
          } catch (error) {
            console.error("❌ خطأ في تحميل الأقسام:", error);
            return [
              { id: "food", name: "مأكولات" },
              { id: "sandwiches", name: "سندوتشات" },
              { id: "drinks", name: "مشروبات" },
            ];
          }
        },

        // المستخدمين
        saveUsers: async (data) => {
          try {
            await db.collection("users").doc("all_users").set({
              data: data,
              lastUpdated: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getUsers: async () => {
          try {
            const doc = await db.collection("users").doc("all_users").get();
            if (doc.exists) return doc.data().data;

            return [
              {
                username: "cashier",
                password: "cashier123",
                role: "cashier",
                name: "الكاشير",
              },
              {
                username: "admin",
                password: "admin123",
                role: "admin",
                name: "المدير",
              },
            ];
          } catch (error) {
            console.error("❌ خطأ في تحميل المستخدمين:", error);
            return [
              {
                username: "cashier",
                password: "cashier123",
                role: "cashier",
                name: "الكاشير",
              },
              {
                username: "admin",
                password: "admin123",
                role: "admin",
                name: "المدير",
              },
            ];
          }
        },

        // الموظفين
        saveEmployees: async (data) => {
          try {
            await db.collection("employees").doc("all_employees").set({
              data: data,
              lastUpdated: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getEmployees: async () => {
          try {
            const doc = await db
              .collection("employees")
              .doc("all_employees")
              .get();
            if (doc.exists) return doc.data().data;

            return [
              {
                id: "1",
                name: "محمد أحمد",
                phone: "01112223344",
                salary: 5000,
                position: "طباخ",
                hireDate: "2023-01-15",
                loans: [],
                vacations: [],
                deductions: [],
                status: "active",
              },
              {
                id: "2",
                name: "أحمد محمد",
                phone: "01098765432",
                salary: 4000,
                position: "مساعد طباخ",
                hireDate: "2023-02-20",
                loans: [],
                vacations: [],
                deductions: [],
                status: "active",
              },
            ];
          } catch (error) {
            console.error("❌ خطأ في تحميل الموظفين:", error);
            return [
              {
                id: "1",
                name: "محمد أحمد",
                phone: "01112223344",
                salary: 5000,
                position: "طباخ",
                hireDate: "2023-01-15",
                loans: [],
                vacations: [],
                deductions: [],
                status: "active",
              },
              {
                id: "2",
                name: "أحمد محمد",
                phone: "01098765432",
                salary: 4000,
                position: "مساعد طباخ",
                hireDate: "2023-02-20",
                loans: [],
                vacations: [],
                deductions: [],
                status: "active",
              },
            ];
          }
        },

        // رقم الفاتورة
        saveInvoiceNumber: async (number, date) => {
          try {
            await db
              .collection("settings")
              .doc("invoice_number")
              .set({
                value: number,
                date: date || new Date().toISOString().split("T")[0],
                lastUpdated: new Date().toISOString(),
              });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getInvoiceNumber: async () => {
          try {
            const doc = await db
              .collection("settings")
              .doc("invoice_number")
              .get();
            const today = new Date().toISOString().split("T")[0];

            if (doc.exists) {
              const data = doc.data();
              return data.date === today ? data.value || 1 : 1;
            }
            return 1;
          } catch (error) {
            console.error("❌ خطأ في تحميل رقم الفاتورة:", error);
            return 1;
          }
        },

        // معلومات المطعم
        saveRestaurantInfo: async (data) => {
          try {
            await db.collection("settings").doc("restaurant_info").set({
              data: data,
              lastUpdated: new Date().toISOString(),
            });
            return { success: true, message: "تم الحفظ بنجاح" };
          } catch (error) {
            return { success: false, message: "فشل الحفظ: " + error.message };
          }
        },

        getRestaurantInfo: async () => {
          try {
            const doc = await db
              .collection("settings")
              .doc("restaurant_info")
              .get();
            if (doc.exists) {
              const data = doc.data().data;
              if (!data.deliveryNumbers) data.deliveryNumbers = [];
              // NEW: ensure deliveryPrices array exists
              if (!data.deliveryPrices)
                data.deliveryPrices = [0, 0, 0, 0, 0, 0];
              return data;
            }
            return {
              name: "كفتة على الفحم",
              number: "1",
              branchName: "الفرع الرئيسي",
              deliveryNumbers: [],
              deliveryPrices: [0, 0, 0, 0, 0, 0], // NEW
            };
          } catch (error) {
            console.error("❌ خطأ في تحميل معلومات المطعم:", error);
            return {
              name: "كفتة على الفحم",
              number: "1",
              branchName: "الفرع الرئيسي",
              deliveryNumbers: [],
              deliveryPrices: [0, 0, 0, 0, 0, 0],
            };
          }
        },
      };

      // ==================== مدير المزامنة (SyncManager) ====================
      const SyncManager = {
        pendingOperations: [],
        isSyncing: false,

        init: function () {
          window.addEventListener("online", () => {
            updateConnectionStatus(true);
            this.syncPendingOperations();
          });

          window.addEventListener("offline", () => {
            updateConnectionStatus(false);
          });

          this.checkConnectionStatus();
        },

        checkConnectionStatus: function () {
          updateConnectionStatus(navigator.onLine);
          if (navigator.onLine) this.syncPendingOperations();
        },

        addPendingOperation: function (type, data) {
          const operation = {
            id: Date.now(),
            type: type,
            data: data,
            timestamp: new Date().toISOString(),
            status: "pending",
            retryCount: 0,
          };

          this.pendingOperations.push(operation);
          if (navigator.onLine) this.syncPendingOperations();
          return operation;
        },

        syncPendingOperations: async function () {
          if (
            this.isSyncing ||
            this.pendingOperations.length === 0 ||
            !navigator.onLine
          )
            return;

          this.isSyncing = true;
          const operationsToSync = [...this.pendingOperations];
          const successfulOperations = [];
          const failedOperations = [];

          for (const operation of operationsToSync) {
            try {
              let success = false;

              switch (operation.type) {
                case "sale":
                  const currentSales = await DataManager.getSales();
                  currentSales.push(operation.data);
                  const salesResult = await DataManager.saveSales(currentSales);
                  success = salesResult.success;
                  break;

                case "expense":
                  const currentExpenses = await DataManager.getExpenses();
                  currentExpenses.push(operation.data);
                  const expensesResult =
                    await DataManager.saveExpenses(currentExpenses);
                  success = expensesResult.success;
                  break;

                case "product":
                  const currentProducts = await DataManager.getProducts();
                  const productIndex = currentProducts.findIndex(
                    (p) => p.id === operation.data.id,
                  );
                  if (productIndex >= 0) {
                    currentProducts[productIndex] = operation.data;
                  } else {
                    currentProducts.push(operation.data);
                  }
                  const productsResult =
                    await DataManager.saveProducts(currentProducts);
                  success = productsResult.success;
                  break;
              }

              if (success) {
                successfulOperations.push(operation.id);
              } else {
                failedOperations.push(operation);
              }
            } catch (error) {
              console.error(`❌ خطأ في مزامنة العملية ${operation.id}:`, error);
              failedOperations.push(operation);
            }
          }

          this.pendingOperations = this.pendingOperations.filter(
            (op) => !successfulOperations.includes(op.id),
          );
          failedOperations.forEach((op) => op.retryCount++);
          this.pendingOperations = this.pendingOperations.filter(
            (op) => op.retryCount < 3,
          );
          this.isSyncing = false;

          if (successfulOperations.length > 0) {
            showNotification(
              `✅ تمت مزامنة ${successfulOperations.length} عملية بنجاح`,
              "success",
            );
          }
          if (failedOperations.length > 0) {
            showNotification(
              `⚠️ فشلت مزامنة ${failedOperations.length} عملية`,
              "warning",
            );
          }
        },
      };

      // ==================== المتغيرات العامة ====================
      let currentUser = null;
      let currentRole = "cashier";
      let products = [];
      let sales = [];
      let expenses = [];
      let orders = [];
      let invoiceItems = [];
      let selectedPaymentMethod = "cash";
      let currentInvoiceNumber = 1;
      let editingProductId = null;
      let currentOrderType = "hall";
      let currentSearchTerm = "";
      let currentDiscountType = "percentage";
      let currentDiscountValue = 0;
      let currentOrdersFilter = "pending";
      let categories = [];
      let employees = [];
      let currentEmployeeAction = "";
      let currentEmployeeId = "";
      let isPrinting = false;
      let users = [];

      let restaurantInfo = {
        name: "كفتة على الفحم",
        number: "1",
        branchName: "الفرع الرئيسي",
        deliveryNumbers: [],
        deliveryPrices: [0, 0, 0, 0, 0, 0], // NEW
      };

      let deliveryPersonnel = [];
      let deliveryOrders = [];
      let currentDeliveryOrder = null;
      let deliveryCustomers = {};

      let currentProductManualIngredients = [];
      let currentQuantity = 1;
      let currentProductForQuantity = null;
      const MAX_QUANTITY = 999;

      let holdInvoices = [];
      let holdInvoicesVisible = false;

      let isGroupedByCategory = false;

      // ==================== دوال المصادقة ====================
      function setRole(role) {
        currentRole = role;
        document
          .querySelectorAll(".role-btn")
          .forEach((btn) => btn.classList.remove("active"));
        event.target.classList.add("active");
      }

      async function login() {
        const username = document.getElementById("username").value.trim();
        const password = document.getElementById("password").value.trim();

        if (!username || !password) {
          showNotification("❌ يرجى ملء جميع الحقول", "error");
          return;
        }

        const users = await DataManager.getUsers();
        const user = users.find(
          (u) => u.username === username && u.password === password,
        );

        if (!user) {
          showNotification("❌ بيانات الدخول غير صحيحة", "error");
          return;
        }

        currentUser = user;
        document.getElementById("loginScreen").style.display = "none";

        if (user.role === "admin") {
          document.getElementById("adminScreen").style.display = "block";
          document.getElementById("adminName").textContent =
            `المدير: ${user.name}`;
          await loadAdminData();
        } else {
          document.getElementById("cashierScreen").style.display = "block";
          document.getElementById("cashierName").textContent =
            `الكاشير: ${user.name}`;
          await loadCashierData();
        }

        showNotification(`✅ مرحباً ${user.name}`, "success");
      }

      function logout() {
        currentUser = null;
        invoiceItems = [];
        selectedPaymentMethod = "cash";
        currentOrderType = "hall";

        document.getElementById("username").value = "";
        document.getElementById("password").value = "";
        document.getElementById("loginScreen").style.display = "flex";
        document.getElementById("cashierScreen").style.display = "none";
        document.getElementById("adminScreen").style.display = "none";

        showNotification("✅ تم تسجيل الخروج بنجاح", "success");
      }

      // ==================== دوال مساعدة عامة ====================
      function showNotification(message, type = "info") {
        const notification = document.createElement("div");
        notification.className = `notification ${type}`;
        notification.innerHTML = `
            ${
              type === "success"
                ? '<i class="fas fa-check-circle"></i>'
                : type === "error"
                  ? '<i class="fas fa-exclamation-circle"></i>'
                  : type === "warning"
                    ? '<i class="fas fa-exclamation-triangle"></i>'
                    : '<i class="fas fa-info-circle"></i>'
            }
            ${message}
        `;
        document.body.appendChild(notification);

        setTimeout(() => {
          notification.style.opacity = "0";
          notification.style.transform = "translateY(-20px)";
          setTimeout(() => notification.remove(), 300);
        }, 2500);
      }

      function updateTime() {
        const now = new Date();
        const timeString = now.toLocaleTimeString("ar-EG", {
          hour: "2-digit",
          minute: "2-digit",
          second: "2-digit",
        });
        const dateString = now.toLocaleDateString("ar-EG", {
          year: "numeric",
          month: "long",
          day: "numeric",
          weekday: "long",
        });

        const cashierTimeElement = document.getElementById("cashierTime");
        const adminTimeElement = document.getElementById("adminTime");

        if (cashierTimeElement)
          cashierTimeElement.textContent = `${dateString} - ${timeString}`;
        if (adminTimeElement)
          adminTimeElement.textContent = `${dateString} - ${timeString}`;
      }

      function updateConnectionStatus(isConnected) {
        const dots = document.querySelectorAll(".connection-dot");
        const texts = document.querySelectorAll('[id^="connectionText"]');

        dots.forEach((dot) => {
          if (isConnected) {
            dot.classList.add("online");
            dot.classList.remove("offline");
          } else {
            dot.classList.add("offline");
            dot.classList.remove("online");
          }
        });

        texts.forEach((text) => {
          text.textContent = isConnected
            ? "متصل بالإنترنت"
            : "غير متصل بالإنترنت";
        });
      }

      function safeCall(functionName, ...args) {
        if (typeof window[functionName] === "function") {
          return window[functionName](...args);
        } else {
          console.error(`❌ الدالة ${functionName} غير معرفة`);
          showNotification(`❌ وظيفة غير متاحة: ${functionName}`, "error");
          return null;
        }
      }

      // ==================== دوال الكاشير الأساسية ====================
      async function loadCashierData() {
        try {
          products = await DataManager.getProducts();
          sales = await DataManager.getSales();
          expenses = await DataManager.getExpenses();
          orders = await DataManager.getOrders();
          categories = await DataManager.getCategories();
          restaurantInfo = await DataManager.getRestaurantInfo();

          currentInvoiceNumber = await DataManager.getInvoiceNumber();

          const savedHoldInvoices = localStorage.getItem("kafta_hold_invoices");
          if (savedHoldInvoices) {
            try {
              holdInvoices = JSON.parse(savedHoldInvoices);
              updateHoldInvoicesUI();
            } catch (e) {
              console.error("خطأ في تحميل الفواتير المعلقة:", e);
              holdInvoices = [];
            }
          }

          updateCategoryButtons();
          displayProducts("all");
          updateTodayStats();
          updateTime();
          setInterval(updateTime, 1000);

          const today = new Date().toISOString().split("T")[0];
          document.getElementById("cashierFilterStartDate").value = today;
          document.getElementById("cashierFilterEndDate").value = today;

          updateCategoryFilterOptions("cashier");
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات الكاشير:", error);
          showNotification("❌ حدث خطأ في تحميل البيانات", "error");
        }
      }

      function updateCategoryButtons() {
        const container = document.getElementById("categoryButtons");
        if (categories.length === 0) {
          container.innerHTML = "";
          return;
        }

        container.innerHTML = categories
          .map(
            (category) =>
              `<button class="btn btn-secondary" onclick="displayProducts('${category.id}')">${category.name}</button>`,
          )
          .join("");
      }

      function displayProducts(category, searchTerm = "") {
        const container = document.getElementById("productsContainer");
        let filtered = products;

        if (category !== "all")
          filtered = filtered.filter((p) => p.category === category);
        if (searchTerm)
          filtered = filtered.filter((p) =>
            p.name.toLowerCase().includes(searchTerm.toLowerCase()),
          );

        if (filtered.length === 0) {
          container.innerHTML =
            '<div class="empty-state"><div class="empty-state-icon"><i class="fas fa-box"></i></div><p>لا توجد منتجات</p></div>';
          return;
        }

        container.innerHTML = filtered
          .map(
            (product) => `
            <div class="product-card">
                <img src="${product.image}" alt="${product.name}" onerror="this.src='https://via.placeholder.com/150'">
                <h4>${product.name}</h4>
                <div class="price">${(product.price || 0).toFixed(2)} جنيه</div>
                <button class="add-btn" onclick="openQuantityModal('${product.id}')">
                    <i class="fas fa-plus"></i> إضافة
                </button>
            </div>
        `,
          )
          .join("");
      }

      function searchProducts() {
        const searchInput = document.getElementById("productSearch");
        currentSearchTerm = searchInput.value;

        let currentCategory = "all";
        document
          .querySelectorAll("#cashierPosTab .btn-secondary")
          .forEach((btn) => {
            if (btn.classList.contains("active")) {
              const text = btn.textContent.trim();
              if (text.includes("جميع")) currentCategory = "all";
              else {
                const foundCategory = categories.find((c) => c.name === text);
                if (foundCategory) currentCategory = foundCategory.id;
              }
            }
          });

        displayProducts(currentCategory, currentSearchTerm);
      }

      function updateTodayStats() {
        const today = new Date();
        today.setHours(0, 0, 0, 0);
        const tomorrow = new Date(today);
        tomorrow.setDate(tomorrow.getDate() + 1);

        const todaySales = sales.filter((s) => {
          const saleDate = new Date(s.date);
          return saleDate >= today && saleDate < tomorrow;
        });

        const todayExpenses = expenses.filter((e) => {
          const expenseDate = new Date(e.date);
          return expenseDate >= today && expenseDate < tomorrow;
        });

        const totalSales = todaySales.reduce(
          (sum, s) => sum + (s.finalTotal || s.total),
          0,
        );
        const totalExpenses = todayExpenses.reduce(
          (sum, e) => sum + e.amount,
          0,
        );
        const netIncome = totalSales - totalExpenses;
        const orderCount = todaySales.length;

        const salesAmountEl = document.getElementById("todaySalesAmount");
        if (salesAmountEl)
          salesAmountEl.textContent = totalSales.toFixed(2) + " جنيه";

        const expensesAmountEl = document.getElementById("todayExpensesAmount");
        if (expensesAmountEl)
          expensesAmountEl.textContent = totalExpenses.toFixed(2) + " جنيه";

        const netAmountEl = document.getElementById("todayNetAmount");
        if (netAmountEl)
          netAmountEl.textContent = netIncome.toFixed(2) + " جنيه";

        const ordersCountEl = document.getElementById("todayOrdersCount");
        if (ordersCountEl) ordersCountEl.textContent = orderCount;
      }

      // ==================== دوال الفاتورة ====================
      function setOrderType(type) {
        currentOrderType = type;
        document.querySelectorAll(".order-type-btn").forEach((btn) => {
          btn.classList.remove("active");
          btn.style.borderColor = "var(--border-color)";
        });
        event.target.classList.add("active");

        const tableNumberContainer =
          document.getElementById("tableNumber").parentElement;
        const deliveryNumberContainer =
          document.getElementById("deliveryNumber").parentElement;
        const customerNameContainer =
          document.getElementById("customerName").parentElement;
        const deliveryLocationSection = document.getElementById(
          "deliveryLocationSection",
        );
        const deliveryZonesContainer = document.getElementById(
          "deliveryZonesContainer",
        );

        tableNumberContainer.style.display = "none";
        deliveryNumberContainer.style.display = "none";
        customerNameContainer.style.display = "none";
        if (deliveryLocationSection) {
          deliveryLocationSection.classList.remove("active");
          deliveryLocationSection.style.display = "none";
        }
        if (deliveryZonesContainer)
          deliveryZonesContainer.style.display = "none";

        // NEW: if switching away from delivery, remove delivery charge item if exists
        if (type !== "delivery") {
          removeDeliveryChargeIfExists();
        }

        switch (type) {
          case "hall":
            tableNumberContainer.style.display = "block";
            event.target.style.borderColor = "#4CAF50";
            break;
          case "takeout":
            customerNameContainer.style.display = "block";
            event.target.style.borderColor = "#2196F3";
            break;
          case "delivery":
            deliveryNumberContainer.style.display = "block";
            customerNameContainer.style.display = "block";
            if (deliveryLocationSection) {
              deliveryLocationSection.style.display = "block";
              deliveryLocationSection.classList.add("active");
            }
            if (deliveryZonesContainer) {
              deliveryZonesContainer.style.display = "block";
              updateDeliveryZoneButtons(); // NEW: create zone buttons
            }
            event.target.style.borderColor = "#FF9800";
            break;
        }
      }

      // NEW: update zone buttons based on saved prices
      function updateDeliveryZoneButtons() {
        const container = document.getElementById("deliveryZoneButtons");
        if (!container) return;
        const prices = restaurantInfo.deliveryPrices || [0, 0, 0, 0, 0, 0];
        let html = "";
        for (let i = 0; i < 6; i++) {
          const zoneNum = i + 1;
          const price = prices[i] || 0;
          html += `
      <button class="zone-btn" data-zone="${zoneNum}" onclick="addOrUpdateDeliveryCharge(${i}, ${price})">
        منطقة ${zoneNum}
        <span class="zone-price">${price} ج</span>
      </button>
    `;
        }
        container.innerHTML = html;
      }
      // NEW: add/update delivery charge item in invoice
      function addOrUpdateDeliveryCharge(zoneIndex, price) {
        if (price <= 0) {
          showNotification("❌ سعر التوصيل لهذه المنطقة غير محدد (0)", "error");
          return;
        }
        const zoneNum = zoneIndex + 1;
        const itemId = `delivery_zone_${zoneNum}`;
        const existingIndex = invoiceItems.findIndex(
          (item) => item.id === itemId,
        );
        const newItem = {
          id: itemId,
          name: `توصيل - منطقة ${zoneNum}`,
          price: price,
          quantity: 1,
          isDelivery: true,
          zone: zoneNum,
        };
        if (existingIndex >= 0) {
          // update price (maybe admin changed price after adding)
          invoiceItems[existingIndex].price = price;
        } else {
          invoiceItems.push(newItem);
        }
        updateInvoiceDisplay();
        // Highlight the zone button as selected (optional)
        document
          .querySelectorAll(".zone-btn")
          .forEach((btn) => btn.classList.remove("active"));
        event.target.classList.add("active");
        showNotification(
          `✅ تم إضافة تكلفة توصيل المنطقة ${zoneNum} (${price} ج)`,
          "success",
        );
      }

      // NEW: remove delivery charge item (used when switching order type)
      function removeDeliveryChargeIfExists() {
        const deliveryItems = invoiceItems.filter((item) => item.isDelivery);
        if (deliveryItems.length > 0) {
          invoiceItems = invoiceItems.filter((item) => !item.isDelivery);
          updateInvoiceDisplay();
        }
      }

      function setDiscountType(type) {
        currentDiscountType = type;
        document
          .querySelectorAll(".discount-type-btn")
          .forEach((btn) => btn.classList.remove("active"));
        event.target.classList.add("active");

        const discountInput = document.getElementById("discountValue");
        if (type === "percentage") {
          discountInput.max = 100;
          discountInput.placeholder = "0%";
        } else {
          discountInput.max = "";
          discountInput.placeholder = "0 جنيه";
        }
        updateInvoiceTotal();
      }

      function updateInvoiceTotal() {
        const discountInput = document.getElementById("discountValue");
        currentDiscountValue = parseFloat(discountInput.value) || 0;
        updateInvoiceDisplay();
      }

      function selectPayment(method) {
        selectedPaymentMethod = method;
        document
          .querySelectorAll(".payment-btn")
          .forEach((btn) => btn.classList.remove("active"));
        event.target.classList.add("active");
      }

      function updateInvoiceDisplay() {
        const container = document.getElementById("invoiceItems");
        if (invoiceItems.length === 0) {
          container.innerHTML =
            '<div class="empty-state"><div class="empty-state-icon"><i class="fas fa-shopping-cart"></i></div><p>لم تضف أي منتجات بعد</p></div>';
          document.getElementById("totalAmount").textContent = "0.00";
          return;
        }

        let total = 0;
        container.innerHTML = invoiceItems
          .map((item, index) => {
            const itemTotal = (item.price || 0) * item.quantity;
            total += itemTotal;
            return `
                <div class="invoice-item" style="animation-delay: ${index * 0.1}s">
                    <div class="invoice-item-info">
                        <div class="invoice-item-name">${item.name}</div>
                        <div class="invoice-item-qty">
                            الكمية: 
                            <button onclick="changeItemQuantity('${item.id}', -1)" title="تقليل الكمية"><i class="fas fa-minus"></i></button>
                            <span style="margin: 0 8px; font-weight: bold;">${item.quantity}</span>
                            <button onclick="changeItemQuantity('${item.id}', 1)" title="زيادة الكمية"><i class="fas fa-plus"></i></button>
                        </div>
                    </div>
                    <div style="display: flex; align-items: center; gap: 10px;">
                        <div class="invoice-item-price">${itemTotal.toFixed(2)} جنيه</div>
                        <button class="invoice-item-remove" onclick="removeFromInvoice('${item.id}')" title="حذف المنتج"><i class="fas fa-trash"></i></button>
                    </div>
                </div>
            `;
          })
          .join("");

        let discountAmount = 0;
        if (currentDiscountValue > 0) {
          if (currentDiscountType === "percentage") {
            discountAmount = total * (currentDiscountValue / 100);
          } else {
            discountAmount = Math.min(currentDiscountValue, total);
          }
        }

        const finalTotal = total - discountAmount;
        document.getElementById("totalAmount").textContent =
          finalTotal.toFixed(2);

        if (invoiceItems.length > 0) {
          const invoicePanel = document.querySelector(".invoice-panel");
          invoicePanel.style.transform = "scale(1.01)";
          setTimeout(() => (invoicePanel.style.transform = "scale(1)"), 200);
        }
      }

      function changeItemQuantity(productId, change) {
        const item = invoiceItems.find((item) => item.id === productId);
        if (item) {
          item.quantity = Math.max(1, item.quantity + change);
          updateInvoiceDisplay();
        }
      }

      function removeFromInvoice(productId) {
        const productName =
          invoiceItems.find((item) => item.id === productId)?.name || "المنتج";
        invoiceItems = invoiceItems.filter((item) => item.id !== productId);
        updateInvoiceDisplay();
        showNotification(`✅ تم حذف ${productName}`, "success");
      }

      function clearInvoice() {
        invoiceItems = [];
        currentDiscountValue = 0;
        currentDiscountType = "percentage";

        document.getElementById("discountValue").value = "";
        document.getElementById("tableNumber").value = "";
        document.getElementById("deliveryNumber").value = "";
        document.getElementById("customerName").value = "";
        document.getElementById("deliveryLocation").value = "";
        document.getElementById("orderNotes").value = "";

        updateInvoiceDisplay();
      }

      function highlightInvoice() {
        const invoicePanel = document.querySelector(".invoice-panel");
        if (invoicePanel) {
          invoicePanel.style.transform = "scale(1.02)";
          invoicePanel.style.boxShadow = "0 8px 25px rgba(255, 107, 53, 0.3)";
          setTimeout(() => {
            invoicePanel.style.transform = "scale(1)";
            invoicePanel.style.boxShadow = "0 4px 12px rgba(0, 0, 0, 0.1)";
          }, 300);
        }
      }

      // ==================== دوال نافذة الكمية ====================
      function openQuantityModal(productId) {
        const product = products.find((p) => p.id === productId);
        if (!product) return;

        currentProductForQuantity = product;
        currentQuantity = 1;

        document.getElementById("modalProductName").textContent = product.name;
        document.getElementById("modalProductPrice").textContent =
          (product.price || 0).toFixed(2) + " جنيه";
        document.getElementById("quantityValue").textContent = currentQuantity;

        document.getElementById("quantityModal").style.display = "flex";
        updateAddButtonState();
      }

      function closeQuantityModal() {
        document.getElementById("quantityModal").style.display = "none";
        currentProductForQuantity = null;
        currentQuantity = 1;
      }

      function addNumber(number) {
        if (currentQuantity === 0) {
          currentQuantity = number;
        } else {
          const newQuantity = parseInt(
            currentQuantity.toString() + number.toString(),
          );
          if (newQuantity <= MAX_QUANTITY) currentQuantity = newQuantity;
        }
        document.getElementById("quantityValue").textContent = currentQuantity;
        updateAddButtonState();
      }

      function addDoubleZero() {
        if (currentQuantity !== 0) {
          const newQuantity = parseInt(currentQuantity.toString() + "00");
          if (newQuantity <= MAX_QUANTITY) currentQuantity = newQuantity;
        }
        document.getElementById("quantityValue").textContent = currentQuantity;
        updateAddButtonState();
      }

      function backspace() {
        if (currentQuantity < 10) {
          currentQuantity = 0;
        } else {
          currentQuantity = Math.floor(currentQuantity / 10);
        }
        document.getElementById("quantityValue").textContent = currentQuantity;
        updateAddButtonState();
      }

      function setQuickQuantity(value) {
        currentQuantity = Math.min(currentQuantity + value, MAX_QUANTITY);
        document.getElementById("quantityValue").textContent = currentQuantity;
        updateAddButtonState();
      }

      function updateAddButtonState() {
        const addButton = document.getElementById("addToInvoiceBtn");
        if (currentQuantity > 0 && currentQuantity <= MAX_QUANTITY) {
          addButton.disabled = false;
          addButton.innerHTML = `<i class="fas fa-plus"></i> إضافة (${currentQuantity}) للفاتورة`;
        } else {
          addButton.disabled = true;
          addButton.innerHTML = `<i class="fas fa-plus"></i> إضافة للفاتورة`;
        }
      }

      function addToInvoiceWithQuantity() {
        if (
          !currentProductForQuantity ||
          currentQuantity <= 0 ||
          currentQuantity > MAX_QUANTITY
        ) {
          showNotification("❌ كمية غير صالحة", "error");
          return;
        }

        const existingItem = invoiceItems.find(
          (item) => item.id === currentProductForQuantity.id,
        );
        if (existingItem) {
          existingItem.quantity += currentQuantity;
        } else {
          invoiceItems.push({
            id: currentProductForQuantity.id,
            name: currentProductForQuantity.name,
            price: currentProductForQuantity.price || 0,
            quantity: currentQuantity,
          });
        }

        updateInvoiceDisplay();
        showNotification(
          `✅ تم إضافة ${currentQuantity} من ${currentProductForQuantity.name}`,
          "success",
        );
        closeQuantityModal();
      }

      // ==================== دوال إتمام البيع والتوصيل ====================
      function checkDeliveryNumber() {
        const deliveryNumber = document
          .getElementById("deliveryNumber")
          .value.trim();
        const customerNameInput = document.getElementById("customerName");
        const deliveryLocationInput =
          document.getElementById("deliveryLocation");

        if (deliveryNumber) {
          // البحث في المبيعات (sales) عن آخر فاتورة بهذا الرقم
          const matchingSales = sales.filter(
            (sale) =>
              sale.deliveryNumber === deliveryNumber &&
              sale.orderType === "delivery",
          );
          if (matchingSales.length > 0) {
            // ترتيب تنازلي حسب التاريخ لآخر فاتورة
            matchingSales.sort((a, b) => new Date(b.date) - new Date(a.date));
            const lastSale = matchingSales[0];

            // تعبئة اسم العميل
            if (lastSale.customerName && lastSale.customerName.trim() !== "") {
              customerNameInput.value = lastSale.customerName;
              customerNameInput.style.backgroundColor = "#e8f5e9";
              customerNameInput.style.border = "2px solid #4CAF50";
            }

            // تعبئة مكان التوصيل
            if (
              lastSale.deliveryLocation &&
              lastSale.deliveryLocation.trim() !== ""
            ) {
              deliveryLocationInput.value = lastSale.deliveryLocation;
              deliveryLocationInput.style.backgroundColor = "#e8f5e9";
              deliveryLocationInput.style.border = "2px solid #4CAF50";
            }

            // اختيارياً: تفعيل منطقة التوصيل إذا كانت موجودة
            if (
              lastSale.deliveryZone !== undefined &&
              lastSale.deliveryZone !== null
            ) {
              // إزالة التحديد من جميع الأزرار ثم تحديد الزر المناسب
              document
                .querySelectorAll(".zone-btn")
                .forEach((btn) => btn.classList.remove("active"));
              const zoneBtn = document.querySelector(
                `.zone-btn[data-zone="${lastSale.deliveryZone}"]`,
              );
              if (zoneBtn) {
                zoneBtn.classList.add("active");
                // يمكن أيضاً إضافة تكلفة التوصيل تلقائياً إذا رغبت، لكن نتركها للمستخدم
              }
            }

            // إزالة التمييز بعد 3 ثواني
            setTimeout(() => {
              customerNameInput.style.backgroundColor = "";
              customerNameInput.style.border = "";
              deliveryLocationInput.style.backgroundColor = "";
              deliveryLocationInput.style.border = "";
            }, 3000);

            showNotification(
              `✅ تم العثور على بيانات سابقة للرقم ${deliveryNumber}`,
              "success",
            );
          } else {
            // لم يتم العثور على بيانات سابقة
            customerNameInput.style.backgroundColor = "";
            customerNameInput.style.border = "";
            deliveryLocationInput.style.backgroundColor = "";
            deliveryLocationInput.style.border = "";
          }
        }
      }

      async function completeSale() {
        const completeBtn = document.querySelector(
          "#cashierPosTab .btn-success",
        ); // زر إتمام البيع
        if (completeBtn.disabled) return; // إذا كان معطلاً بالفعل لا تفعل شيء
        if (invoiceItems.length === 0) {
          showNotification("❌ يرجى إضافة منتجات قبل إتمام البيع", "error");
          return;
        }

        // تعطيل الزر لمنع التكرار
        completeBtn.disabled = true;
        completeBtn.innerHTML =
          '<i class="fas fa-spinner fa-spin"></i> جاري الإتمام...';

        try {
          const total = invoiceItems.reduce(
            (sum, item) => sum + (item.price || 0) * item.quantity,
            0,
          );

          let discountAmount = 0;
          if (currentDiscountValue > 0) {
            if (currentDiscountType === "percentage") {
              discountAmount = total * (currentDiscountValue / 100);
            } else {
              discountAmount = Math.min(currentDiscountValue, total);
            }
          }

          const finalTotal = total - discountAmount;
          const tableNumber = document
            .getElementById("tableNumber")
            .value.trim();
          const deliveryNumber = document
            .getElementById("deliveryNumber")
            .value.trim();
          let customerName = document
            .getElementById("customerName")
            .value.trim();
          const orderNotes = document.getElementById("orderNotes").value.trim();
          const deliveryLocation = document
            .getElementById("deliveryLocation")
            .value.trim();

          // NEW: extract delivery zone info from invoice items
          let deliveryZone = null;
          let deliveryPrice = 0;
          const deliveryItem = invoiceItems.find((item) => item.isDelivery);
          if (deliveryItem) {
            deliveryZone = deliveryItem.zone;
            deliveryPrice = deliveryItem.price;
          }

          if (
            currentOrderType === "delivery" &&
            deliveryNumber &&
            customerName
          ) {
            deliveryCustomers[deliveryNumber] = customerName;
            localStorage.setItem(
              "kafta_delivery_customers",
              JSON.stringify(deliveryCustomers),
            );

            try {
              await db
                .collection("delivery_customers")
                .doc(deliveryNumber)
                .set({
                  name: customerName,
                  lastUpdated: new Date().toISOString(),
                  lastOrderDate: new Date().toISOString(),
                });
            } catch (error) {
              console.log("لم يتم حفظ العميل في Firebase:", error);
            }
          }

          const sale = {
            id: Date.now().toString(),
            invoiceNumber: currentInvoiceNumber,
            date: new Date().toISOString(),
            items: [...invoiceItems],
            total: total,
            discount: discountAmount,
            finalTotal: finalTotal,
            paymentMethod: selectedPaymentMethod,
            orderType: currentOrderType,
            tableNumber: tableNumber,
            deliveryNumber: deliveryNumber,
            customerName: customerName,
            deliveryLocation: deliveryLocation,
            deliveryZone: deliveryZone, // NEW
            deliveryPrice: deliveryPrice, // NEW
            orderNotes: orderNotes,
            cashier: currentUser.name,
            status: "completed",
          };

          sales.push(sale);
          const result = await DataManager.saveSales(sales);

          if (result.success) {
            showNotification(
              `✅ تم إتمام البيع برقم فاتورة ${String(sale.invoiceNumber).padStart(4, "0")}`,
              "success",
            );

            if (currentOrderType === "delivery") {
              const order = {
                ...sale,
                status: "pending",
                deliveryPersonnelName: "",
                deliveryPaymentMethod: "",
                deliveryPersonnelUpdatedAt: null,
                deliveryPaymentUpdatedAt: null,
                deliveryPersonnelUpdatedBy: null,
                deliveryPaymentUpdatedBy: null,
                statusUpdatedAt: new Date().toISOString(),
                statusUpdatedBy: currentUser.name,
              };

              orders.push(order);
              deliveryOrders.push(order);

              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
              await DataManager.saveOrders(orders);
              await DataManager.saveDeliveryOrders(deliveryOrders);
            }

            const today = new Date().toISOString().split("T")[0];
            currentInvoiceNumber++;
            await DataManager.saveInvoiceNumber(currentInvoiceNumber, today);

            updateTodayStats();

            // طباعة الفاتورة مباشرة بعد النجاح
            showPrintModal(sale);

            invoiceItems = [];
            currentDiscountValue = 0;
            document.getElementById("discountValue").value = "";
            document.getElementById("tableNumber").value = "";
            document.getElementById("deliveryNumber").value = "";
            document.getElementById("customerName").value = "";
            document.getElementById("deliveryLocation").value = "";
            document.getElementById("orderNotes").value = "";
            updateInvoiceDisplay();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في إتمام البيع:", error);
          showNotification("❌ حدث خطأ في إتمام البيع", "error");
        } finally {
          // إعادة تمكين الزر بعد الانتهاء
          completeBtn.disabled = false;
          completeBtn.innerHTML =
            '<i class="fas fa-check-circle"></i> إتمام البيع';
        }
      }

      // دالة طباعة تقرير الكاشير
      function printCashierReport() {
        const startDate = document.getElementById(
          "cashierFilterStartDate",
        ).value;
        const endDate = document.getElementById("cashierFilterEndDate").value;
        const paymentMethod = document.getElementById(
          "cashierFilterPayment",
        )?.value;
        const orderType = document.getElementById(
          "cashierFilterOrderType",
        )?.value;

        let title = `تقرير المبيعات من ${startDate || "البداية"} إلى ${endDate || "النهاية"}`;
        if (paymentMethod && paymentMethod !== "all")
          title += ` - طريقة الدفع: ${getPaymentMethodName(paymentMethod)}`;
        if (orderType && orderType !== "all")
          title += ` - نوع الطلب: ${getOrderTypeName(orderType)}`;

        const totalEl =
          document.getElementById("cashierReportTotal")?.innerText || "0";
        const countEl =
          document.getElementById("cashierReportCount")?.innerText || "0";
        const avgEl =
          document.getElementById("cashierReportAverage")?.innerText || "0";
        const expEl =
          document.getElementById("cashierReportExpenses")?.innerText || "0";
        const netEl =
          document.getElementById("cashierReportNet")?.innerText || "0";

        const tableHtml =
          document.getElementById("cashierReportTableBody")?.parentElement
            ?.outerHTML || "";

        const printWindow = window.open("", "", "width=900,height=700");
        const html = `
    <!DOCTYPE html>
    <html dir="rtl">
    <head>
      <meta charset="UTF-8">
      <title>تقرير الكاشير</title>
      <style>
        body { font-family: Arial; padding: 20px; }
        .header { text-align: center; margin-bottom: 30px; }
        .report-logo { width: 100px; height: 100px; border-radius: 50%; object-fit: cover; }
        .summary { display: grid; grid-template-columns: repeat(5,1fr); gap: 10px; margin: 20px 0; }
        .summary-card { background: #f8f9fa; padding: 15px; border-radius: 8px; text-align: center; }
        .summary-card h4 { margin: 0 0 5px; color: #666; font-size: 14px; }
        .summary-card .value { font-size: 18px; font-weight: bold; color: #FF6B35; }
        table { width: 100%; border-collapse: collapse; margin-top: 20px; }
        th { background: #FF6B35; color: white; padding: 10px; }
        td { border: 1px solid #ddd; padding: 8px; text-align: center; }
        .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); }
        .signature { display: flex; justify-content: space-between; margin-top: 40px; }
        .signature-box { width: 45%; text-align: center; border-top: 2px solid #333; padding-top: 10px; }
      </style>
    </head>
    <body>
      <div class="header">
        <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
        <h2>🍖 ${restaurantInfo.name}</h2>
        <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
        <h4>${title}</h4>
        <p>المستخدم: ${currentUser?.name || "غير محدد"} | التاريخ: ${new Date().toLocaleDateString("ar-EG")}</p>
      </div>
      
      <div class="summary">
        <div class="summary-card"><h4>إجمالي المبيعات</h4><div class="value">${totalEl}</div></div>
        <div class="summary-card"><h4>عدد الفواتير</h4><div class="value">${countEl}</div></div>
        <div class="summary-card"><h4>متوسط الفاتورة</h4><div class="value">${avgEl}</div></div>
        <div class="summary-card"><h4>المصاريف</h4><div class="value">${expEl}</div></div>
        <div class="summary-card"><h4>صافي الدخل</h4><div class="value">${netEl}</div></div>
      </div>
      
      ${tableHtml}
      
      <div class="signature">
        <div class="signature-box"><p>الكاشير</p><p>${currentUser?.name || "...................."}</p></div>
        <div class="signature-box"><p>المدير</p><p>....................</p></div>
      </div>
      <div class="watermark">amaryasser408@gmail.com</div>
    </body>
    </html>
  `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      // دالة طباعة المنتجات الأكثر مبيعاً
      function printTopProductsReport() {
        const tableHtml =
          document.getElementById("cashierTopProductsBody")?.parentElement
            ?.outerHTML || "";
        if (!tableHtml) {
          showNotification("لا توجد بيانات للطباعة", "warning");
          return;
        }
        const printWindow = window.open("", "", "width=800,height=600");
        const html = `
    <!DOCTYPE html>
    <html dir="rtl">
    <head>
      <meta charset="UTF-8">
      <title>المنتجات الأكثر مبيعاً</title>
      <style>
        body { font-family: Arial; padding: 20px; }
        h2 { text-align: center; color: #FF6B35; }
        table { width: 100%; border-collapse: collapse; margin-top: 20px; }
        th { background: #FF6B35; color: white; padding: 10px; }
        td { border: 1px solid #ddd; padding: 8px; text-align: center; }
        .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); }
      </style>
    </head>
    <body>
      <h2>🍖 ${restaurantInfo.name} - المنتجات الأكثر مبيعاً</h2>
      <p style="text-align:center">المستخدم: ${currentUser?.name || "غير محدد"} | التاريخ: ${new Date().toLocaleDateString("ar-EG")}</p>
      ${tableHtml}
      <div class="watermark">amaryasser408@gmail.com</div>
    </body>
    </html>
  `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      // دالة تصدير المنتجات الأكثر مبيعاً إلى Excel
      function exportTopProductsToExcel() {
        try {
          const table = document.getElementById(
            "cashierTopProductsBody",
          )?.parentElement;
          if (!table) {
            showNotification("لا توجد بيانات للتصدير", "error");
            return;
          }
          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المنتجات_الأكثر_مبيعاً");
          XLSX.writeFile(
            wb,
            `المنتجات_الأكثر_مبيعاً_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير التقرير بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في التصدير:", error);
          showNotification("❌ حدث خطأ في التصدير", "error");
        }
      }

      // ==================== دوال الفواتير المعلقة (Hold Invoices) ====================
      function toggleHoldInvoices() {
        holdInvoicesVisible = !holdInvoicesVisible;
        const section = document.getElementById("holdInvoicesSection");
        const icon = document.getElementById("holdInvoicesToggleIcon");

        if (holdInvoicesVisible) {
          section.classList.add("active");
          icon.className = "fas fa-chevron-up";
          updateHoldInvoicesUI();
        } else {
          section.classList.remove("active");
          icon.className = "fas fa-chevron-down";
        }
      }

      function holdInvoice() {
        if (invoiceItems.length === 0) {
          showNotification("❌ لا يمكن تعليق فاتورة فارغة", "error");
          return;
        }

        const total = invoiceItems.reduce(
          (sum, item) => sum + (item.price || 0) * item.quantity,
          0,
        );

        let discountAmount = 0;
        if (currentDiscountValue > 0) {
          if (currentDiscountType === "percentage") {
            discountAmount = total * (currentDiscountValue / 100);
          } else {
            discountAmount = Math.min(currentDiscountValue, total);
          }
        }

        const finalTotal = total - discountAmount;
        const tableNumber = document.getElementById("tableNumber").value.trim();
        const deliveryNumber = document
          .getElementById("deliveryNumber")
          .value.trim();
        const customerName = document
          .getElementById("customerName")
          .value.trim();
        const orderNotes = document.getElementById("orderNotes").value.trim();
        const deliveryLocation = document
          .getElementById("deliveryLocation")
          .value.trim();

        const holdInvoice = {
          id: Date.now().toString(),
          date: new Date().toISOString(),
          time: new Date().toLocaleTimeString("en-US", {
            hour: "2-digit",
            minute: "2-digit",
          }),
          items: [...invoiceItems],
          total: total,
          discount: discountAmount,
          discountType: currentDiscountType,
          discountValue: currentDiscountValue,
          finalTotal: finalTotal,
          paymentMethod: selectedPaymentMethod,
          orderType: currentOrderType,
          tableNumber: tableNumber,
          deliveryNumber: deliveryNumber,
          customerName: customerName,
          deliveryLocation: deliveryLocation,
          orderNotes: orderNotes,
          cashier: currentUser.name,
        };

        holdInvoices.push(holdInvoice);
        localStorage.setItem(
          "kafta_hold_invoices",
          JSON.stringify(holdInvoices),
        );
        updateHoldInvoicesUI();
        clearInvoice();
        showNotification("✅ تم تعليق الفاتورة بنجاح", "success");

        if (!holdInvoicesVisible) toggleHoldInvoices();
      }

      function updateHoldInvoicesUI() {
        const container = document.getElementById("holdInvoicesContainer");
        const countElement = document.getElementById("holdInvoicesCount");

        countElement.textContent = holdInvoices.length;

        if (holdInvoices.length === 0) {
          container.innerHTML =
            '<div class="empty-hold-invoices">لا توجد فواتير معلقة حالياً</div>';
          return;
        }

        const sortedInvoices = [...holdInvoices].sort(
          (a, b) => new Date(b.date) - new Date(a.date),
        );

        container.innerHTML = sortedInvoices
          .map(
            (invoice) => `
            <div class="hold-invoice-card">
                <div class="hold-invoice-header">
                    <div class="hold-invoice-number">فاتورة معلقة</div>
                    <div class="hold-invoice-time">${invoice.time}</div>
                </div>
                <div class="hold-invoice-body">
                    <div class="hold-invoice-items">
                        ${invoice.items
                          .map(
                            (item) => `
                            <div class="hold-invoice-item">
                                <div class="hold-invoice-item-name">
                                    ${item.name} <span class="hold-invoice-item-quantity">(${item.quantity})</span>
                                </div>
                                <div class="hold-invoice-item-price">${((item.price || 0) * item.quantity).toFixed(2)} جنيه</div>
                            </div>
                        `,
                          )
                          .join("")}
                    </div>
                </div>
                <div class="hold-invoice-footer">
                    <div class="hold-invoice-total">الإجمالي: ${invoice.finalTotal.toFixed(2)} جنيه</div>
                    <div class="hold-invoice-actions">
                        <button class="btn-resume" onclick="resumeHoldInvoice('${invoice.id}')"><i class="fas fa-play"></i> استرجاع</button>
                        <button class="btn-delete" onclick="deleteHoldInvoice('${invoice.id}')"><i class="fas fa-trash"></i> حذف</button>
                    </div>
                </div>
            </div>
        `,
          )
          .join("");
      }

      function resumeHoldInvoice(invoiceId) {
        const holdInvoice = holdInvoices.find((inv) => inv.id === invoiceId);
        if (!holdInvoice) {
          showNotification("❌ لم يتم العثور على الفاتورة المعلقة", "error");
          return;
        }

        invoiceItems = [...holdInvoice.items];
        currentDiscountType = holdInvoice.discountType;
        currentDiscountValue = holdInvoice.discountValue;
        selectedPaymentMethod = holdInvoice.paymentMethod;
        currentOrderType = holdInvoice.orderType;

        document.getElementById("tableNumber").value =
          holdInvoice.tableNumber || "";
        document.getElementById("deliveryNumber").value =
          holdInvoice.deliveryNumber || "";
        document.getElementById("customerName").value =
          holdInvoice.customerName || "";
        document.getElementById("deliveryLocation").value =
          holdInvoice.deliveryLocation || "";
        document.getElementById("orderNotes").value =
          holdInvoice.orderNotes || "";
        document.getElementById("discountValue").value =
          holdInvoice.discountValue || "";

        updateInvoiceDisplay();
        setOrderType(holdInvoice.orderType);
        selectPayment(holdInvoice.paymentMethod);

        deleteHoldInvoice(invoiceId);
        showNotification("✅ تم استرجاع الفاتورة بنجاح", "success");
        document
          .getElementById("invoicePanel")
          .scrollIntoView({ behavior: "smooth" });
      }

      function deleteHoldInvoice(invoiceId) {
        holdInvoices = holdInvoices.filter((inv) => inv.id !== invoiceId);
        localStorage.setItem(
          "kafta_hold_invoices",
          JSON.stringify(holdInvoices),
        );
        updateHoldInvoicesUI();
        showNotification("✅ تم حذف الفاتورة المعلقة", "success");
      }

      // ==================== دوال المصاريف ====================
      function openExpenseModal() {
        document.getElementById("expenseModal").style.display = "flex";
        document.getElementById("expenseModalAmount").value = "";
        document.getElementById("expenseModalDescription").value = "";
      }

      function closeExpenseModal() {
        document.getElementById("expenseModal").style.display = "none";
      }

      async function saveExpense() {
        const amount = parseFloat(
          document.getElementById("expenseModalAmount").value,
        );
        const description = document
          .getElementById("expenseModalDescription")
          .value.trim();

        if (!amount || amount <= 0) {
          showNotification("❌ يرجى إدخال مبلغ صحيح", "error");
          return;
        }

        const expense = {
          id: Date.now().toString(),
          amount: amount,
          description: description || "مصروف غير محدد",
          date: new Date().toISOString(),
          user: currentUser.name,
        };

        try {
          expenses.push(expense);
          const result = await DataManager.saveExpenses(expenses);

          if (result.success) {
            showNotification(
              `✅ تم تسجيل مصروف بقيمة ${amount.toFixed(2)} جنيه`,
              "success",
            );
            updateTodayStats();
            closeExpenseModal();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في حفظ المصروف:", error);
          showNotification("❌ حدث خطأ في حفظ المصروف", "error");
        }
      }

      // ==================== دوال التقارير ====================

      async function loadCashierReport() {
        console.log("🔄 بدء تحميل تقرير الكاشير...");

        // الحصول على عناصر حقلي التاريخ
        const startDateInput = document.getElementById(
          "cashierFilterStartDate",
        );
        const endDateInput = document.getElementById("cashierFilterEndDate");
        const today = new Date().toISOString().split("T")[0];

        // تعيين تاريخ اليوم فقط إذا كانت الحقول فارغة (لأول مرة)
        if (!startDateInput.value) {
          startDateInput.value = today;
        }
        if (!endDateInput.value) {
          endDateInput.value = today;
        }

        // الحصول على القيم المدخلة (قد تكون مختلفة عن اليوم)
        const startDate = startDateInput.value;
        const endDate = endDateInput.value;
        const paymentMethod = document.getElementById(
          "cashierFilterPayment",
        )?.value;
        const orderType = document.getElementById(
          "cashierFilterOrderType",
        )?.value;
        const categoryId = document.getElementById(
          "cashierFilterCategory",
        )?.value;

        console.log("📅 التواريخ المدخلة:", { startDate, endDate });

        if (!startDate || !endDate) {
          showNotification("❌ يرجى تحديد تاريخ البداية والنهاية", "error");
          return;
        }

        let filteredSales = [...sales];

        // فلترة حسب التاريخ
        if (startDate && endDate) {
          filteredSales = filteredSales.filter((s) => {
            if (!s || !s.date) return false;
            const saleDate = s.date.split("T")[0];
            return saleDate >= startDate && saleDate <= endDate;
          });
        }

        // فلترة حسب طريقة الدفع
        if (paymentMethod && paymentMethod !== "all") {
          filteredSales = filteredSales.filter(
            (s) => s.paymentMethod === paymentMethod,
          );
        }

        // فلترة حسب نوع الطلب
        if (orderType && orderType !== "all") {
          filteredSales = filteredSales.filter(
            (s) => s.orderType === orderType,
          );
        }

        // فلترة حسب الكاشير الحالي
        if (currentUser && currentUser.name) {
          filteredSales = filteredSales.filter(
            (s) => s.cashier === currentUser.name,
          );
        }

        // فلترة حسب القسم إذا تم اختياره
        if (categoryId && categoryId !== "all" && products.length > 0) {
          filteredSales = filteredSales.filter((s) =>
            s.items?.some((item) => {
              const product = products.find((p) => p.id === item.id);
              return product && product.category === categoryId;
            }),
          );
        }

        // فلترة المصاريف
        let filteredExpenses = [...expenses];
        if (startDate && endDate) {
          filteredExpenses = filteredExpenses.filter((e) => {
            if (!e || !e.date) return false;
            const expenseDate = e.date.split("T")[0];
            return expenseDate >= startDate && expenseDate <= endDate;
          });
        }

        if (currentUser && currentUser.name) {
          filteredExpenses = filteredExpenses.filter(
            (e) => e.user === currentUser.name,
          );
        }

        // تحديث واجهة المستخدم
        updateCashierReportUI(filteredSales, filteredExpenses);

        if (filteredSales.length === 0) {
          showNotification("⚠️ لا توجد مبيعات في هذه الفترة", "warning");
        } else {
          showNotification(
            `✅ تم عرض ${filteredSales.length} فاتورة`,
            "success",
          );
        }
      }

      // ==================== دوال الدليفري للمستخدم ====================
      async function loadUserDeliveryData() {
        try {
          if (navigator.onLine) {
            // تحميل من Firebase أولاً
            const firebaseOrders = await DataManager.getDeliveryOrders();
            if (firebaseOrders && firebaseOrders.length > 0) {
              deliveryOrders = firebaseOrders;
              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
            } else {
              // إذا كانت Firebase فارغة، استخدم localStorage
              const savedDeliveryOrders = localStorage.getItem(
                "kafta_delivery_orders",
              );
              if (savedDeliveryOrders)
                deliveryOrders = JSON.parse(savedDeliveryOrders);
            }

            // تحميل الموصلين
            const firebasePersonnel = await DataManager.getDeliveryPersonnel();
            if (firebasePersonnel && firebasePersonnel.length > 0) {
              deliveryPersonnel = firebasePersonnel;
              localStorage.setItem(
                "kafta_delivery_personnel",
                JSON.stringify(deliveryPersonnel),
              );
            } else {
              const savedPersonnel = localStorage.getItem(
                "kafta_delivery_personnel",
              );
              if (savedPersonnel)
                deliveryPersonnel = JSON.parse(savedPersonnel);
            }
          } else {
            // إذا كان غير متصل، استخدم localStorage
            const savedDeliveryOrders = localStorage.getItem(
              "kafta_delivery_orders",
            );
            if (savedDeliveryOrders)
              deliveryOrders = JSON.parse(savedDeliveryOrders);
            const savedPersonnel = localStorage.getItem(
              "kafta_delivery_personnel",
            );
            if (savedPersonnel) deliveryPersonnel = JSON.parse(savedPersonnel);
          }

          // تعيين التواريخ الافتراضية
          const today = new Date().toISOString().split("T")[0];
          document.getElementById("userDeliveryStartDate").value = today;
          document.getElementById("userDeliveryEndDate").value = today;

          updateUserDeliveryPersonnelSelect();
          loadUserDeliveryOrders();
          updateDeliveryStats();

          showNotification("✅ تم تحميل بيانات الدليفري", "success");
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات الدليفري:", error);
          showNotification("❌ حدث خطأ في تحميل بيانات الدليفري", "error");
        }
      }

      function updateUserDeliveryPersonnelSelect() {
        const select = document.getElementById("userDeliveryPersonnel");
        if (!select) return;

        select.innerHTML = '<option value="all">جميع الموصلين</option>';
        deliveryPersonnel.forEach((person) => {
          const option = document.createElement("option");
          option.value = person.id;
          option.textContent = `${person.name} (${person.phone})`;
          select.appendChild(option);
        });
      }

      function updateDeliveryStats() {
        const today = new Date();
        today.setHours(0, 0, 0, 0);
        const tomorrow = new Date(today);
        tomorrow.setDate(tomorrow.getDate() + 1);

        const todayOrders = deliveryOrders.filter((order) => {
          const orderDate = new Date(order.date);
          return orderDate >= today && orderDate < tomorrow;
        });

        const pendingOrders = deliveryOrders.filter(
          (order) =>
            order.status === "pending" || order.status === "delivering",
        );
        const deliveredToday = todayOrders.filter(
          (order) => order.status === "delivered",
        );
        const totalSales = todayOrders.reduce(
          (sum, order) => sum + (order.finalTotal || 0),
          0,
        );

        document.getElementById("todayDeliveryCount").textContent =
          todayOrders.length;
        document.getElementById("pendingDeliveryCountStat").textContent =
          pendingOrders.length;
        document.getElementById("deliveredCountStat").textContent =
          deliveredToday.length;
        document.getElementById("todayDeliverySales").textContent =
          totalSales.toFixed(2) + " جنيه";

        const badge = document.getElementById("pendingDeliveryCount");
        if (badge) {
          if (pendingOrders.length > 0) {
            badge.style.display = "inline";
            badge.textContent = pendingOrders.length;
          } else {
            badge.style.display = "none";
          }
        }
      }

      function loadUserDeliveryOrders() {
        const startDate = document.getElementById(
          "userDeliveryStartDate",
        ).value;
        const endDate = document.getElementById("userDeliveryEndDate").value;
        const status = document.getElementById("userDeliveryStatus").value;
        const personnelId = document.getElementById(
          "userDeliveryPersonnel",
        ).value;

        let filteredOrders = [...deliveryOrders];

        if (startDate && endDate) {
          const start = new Date(startDate);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDate);
          end.setHours(23, 59, 59, 999);

          filteredOrders = filteredOrders.filter((order) => {
            const orderDate = new Date(order.date);
            return orderDate >= start && orderDate <= end;
          });
        }

        if (status !== "all")
          filteredOrders = filteredOrders.filter(
            (order) => order.status === status,
          );
        if (personnelId !== "all")
          filteredOrders = filteredOrders.filter(
            (order) => order.deliveryPersonnelId === personnelId,
          );

        filteredOrders.sort((a, b) => new Date(b.date) - new Date(a.date));
        displayUserDeliveryOrders(filteredOrders);
      }

      function displayUserDeliveryOrders(orders) {
        const container = document.getElementById("userDeliveryOrdersList");
        if (!container) {
          console.error("❌ عنصر userDeliveryOrdersList غير موجود");
          return;
        }

        if (orders.length === 0) {
          container.innerHTML = `
      <div class="empty-state">
        <div class="empty-state-icon"><i class="fas fa-motorcycle"></i></div>
        <p>لا توجد طلبات توصيل في هذه الفترة</p>
      </div>
    `;
          return;
        }

        let html = `
    <div style="overflow-x: auto; margin-top: 15px;">
      <table class="products-table" style="width: 100%; font-size: 13px;">
        <thead>
          <tr>
            <th>رقم الفاتورة</th>
            <th>التاريخ والوقت</th>
            <th>رقم التوصيل</th>
            <th>العميل</th>
            <th>مكان التوصيل</th>
            <th>الموصل</th>
            <th>طريقة الدفع</th>
            <th>الحالة</th>
            <th>منطقة التوصيل</th>
            <th>الإجمالي</th>
            <th>الإجراءات</th>
          </tr>
        </thead>
        <tbody>
  `;

        orders.forEach((order) => {
          const statusClass = getDeliveryStatusClass(order.status);
          const statusName = getDeliveryStatusName(order.status);
          const paymentMethodName =
            getDeliveryPaymentMethodName(order.deliveryPaymentMethod) ||
            "غير محدد";

          html += `
      <tr>
        <td style="font-weight: bold;">${String(order.invoiceNumber).padStart(4, "0")}</td>
        <td>${new Date(order.date).toLocaleDateString("en-GB")}<br><small>${new Date(order.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</small></td>
        <td>${order.deliveryNumber || "-"}</td>
        <td>${order.customerName || "-"}</td>
        <td>${order.deliveryLocation || "-"}</td>
        <td>
          <input type="text" id="personnel-name-${order.id}" value="${order.deliveryPersonnelName || ""}" 
                 placeholder="اسم الموصل" 
                 style="width: 100px; padding: 4px; border: 1px solid #ddd; border-radius: 4px;"
                 onchange="saveDeliveryPersonnelNameDirect('${order.id}', this.value)">
        </td>
        <td>
          <select id="payment-${order.id}" style="width: 80px; padding: 4px; border: 1px solid #ddd; border-radius: 4px;" 
                  onchange="savePaymentMethodDirect('${order.id}', this.value)">
            <option value="">--</option>
            <option value="cash" ${order.deliveryPaymentMethod === "cash" ? "selected" : ""}>كاش</option>
            <option value="bank" ${order.deliveryPaymentMethod === "bank" ? "selected" : ""}>بنكك</option>
            <option value="foori" ${order.deliveryPaymentMethod === "foori" ? "selected" : ""}>فوري</option>
            <option value="okash" ${order.deliveryPaymentMethod === "okash" ? "selected" : ""}>أوكاش</option>
            <option value="sahel" ${order.deliveryPaymentMethod === "sahel" ? "selected" : ""}>ساهل</option>
          </select>
        </td>
        <td>
          <select id="status-${order.id}" style="width: 100px; padding: 4px; border: 1px solid #ddd; border-radius: 4px;">
            <option value="pending" ${order.status === "pending" ? "selected" : ""}>🟡 انتظار</option>
            <option value="delivering" ${order.status === "delivering" ? "selected" : ""}>🔵 قيد التوصيل</option>
            <option value="delivered" ${order.status === "delivered" ? "selected" : ""}>✅ تم</option>
            <option value="cancelled" ${order.status === "cancelled" ? "selected" : ""}>❌ ملغي</option>
          </select>
        </td>
        <td>${order.deliveryZone ? `منطقة ${order.deliveryZone} (${order.deliveryPrice || 0} ج)` : "-"}</td>
        <td style="color: var(--secondary-color); font-weight: bold;">${(order.finalTotal || 0).toFixed(2)}</td>
        <td>
          <div style="display: flex; gap: 4px; flex-wrap: wrap;">
            <button onclick="viewDeliveryOrderDetails('${order.id}')" style="padding: 4px 8px; background: #2196F3; color: white; border: none; border-radius: 4px; cursor: pointer;" title="عرض التفاصيل"><i class="fas fa-eye"></i></button>
            <button onclick="updateDeliveryOrderComplete('${order.id}')" style="padding: 4px 8px; background: #4CAF50; color: white; border: none; border-radius: 4px; cursor: pointer;" title="حفظ"><i class="fas fa-save"></i></button>
            <button onclick="markAsDeliveredComplete('${order.id}')" style="padding: 4px 8px; background: #2196F3; color: white; border: none; border-radius: 4px; cursor: pointer;" title="تم التوصيل"><i class="fas fa-check"></i></button>
            <button onclick="printSingleDeliveryInvoice('${order.id}')" style="padding: 4px 8px; background: #607D8B; color: white; border: none; border-radius: 4px; cursor: pointer;" title="طباعة"><i class="fas fa-print"></i></button>
          </div>
        </td>
      </tr>
    `;
        });

        html += `
        </tbody>
      </table>
    </div>
  `;

        container.innerHTML = html;
      }
      // ==================== دوال مساعدة للدليفري ====================
      function getDeliveryStatusClass(status) {
        const classes = {
          pending: "pending",
          delivering: "preparing",
          delivered: "delivered",
          cancelled: "cancelled",
        };
        return classes[status] || "pending";
      }

      function getDeliveryStatusName(status) {
        const names = {
          pending: "في انتظار التوصيل",
          delivering: "قيد التوصيل",
          delivered: "تم التوصيل",
          cancelled: "ملغي",
        };
        return names[status] || status;
      }

      function getDeliveryPaymentMethodName(method) {
        const methods = {
          cash: "💵 كاش",
          bank: "🏦 بنكك",
          foori: "📱 فوري",
          okash: "💳 أوكاش",
          sahel: "📲 ساهل",
        };
        return methods[method] || method || "غير محدد";
      }

      function getPersonnelName(personnelId) {
        if (!personnelId) return "غير معين";
        const person = deliveryPersonnel.find((p) => p.id === personnelId);
        return person ? person.name : "غير معين";
      }

      function getStatusColor(status) {
        const colors = {
          pending: "#FFC107",
          delivering: "#2196F3",
          delivered: "#4CAF50",
          cancelled: "#f44336",
        };
        return colors[status] || "#666";
      }

      function getPaymentMethodColor(method) {
        const colors = {
          cash: "#4CAF50",
          bank: "#2196F3",
          foori: "#FF9800",
          okash: "#9C27B0",
          sahel: "#00BCD4",
        };
        return colors[method] || "#9E9E9E";
      }

      // ==================== دوال الحفظ المباشر للدليفري ====================
      async function saveDeliveryPersonnelNameDirect(orderId, personnelName) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) return;

        order.deliveryPersonnelName = personnelName.trim();
        order.deliveryPersonnelUpdatedAt = new Date().toISOString();
        order.deliveryPersonnelUpdatedBy = currentUser
          ? currentUser.name
          : "الكاشير";

        if (navigator.onLine) {
          try {
            const result = await DataManager.saveDeliveryOrders(deliveryOrders);
            if (result.success) {
              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
              showNotification(`✅ تم حفظ الموصل: ${personnelName}`, "success");
              await loadUserDeliveryData();
            } else {
              showNotification(`❌ فشل حفظ الموصل: ${result.message}`, "error");
            }
          } catch (error) {
            console.error("❌ فشل حفظ اسم الموصل:", error);
            showNotification("❌ حدث خطأ في حفظ اسم الموصل", "error");
          }
        } else {
          // إضافة العملية إلى قائمة المزامنة
          SyncManager.addPendingOperation("delivery", order);
          localStorage.setItem(
            "kafta_delivery_orders",
            JSON.stringify(deliveryOrders),
          );
          showNotification("⚠️ أنت غير متصل، سيتم المزامنة لاحقًا", "warning");
        }
      }

      function savePaymentMethodDirect(orderId, paymentMethod) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) return;

        order.deliveryPaymentMethod = paymentMethod;
        order.deliveryPaymentUpdatedAt = new Date().toISOString();
        order.deliveryPaymentUpdatedBy = currentUser
          ? currentUser.name
          : "الكاشير";

        DataManager.saveDeliveryOrders(deliveryOrders)
          .then((result) => {
            if (result.success) {
              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
              const methodName = getDeliveryPaymentMethodName(paymentMethod);
              showNotification(
                `✅ تم حفظ طريقة الدفع: ${methodName}`,
                "success",
              );
              loadUserDeliveryData(); // إعادة تحميل البيانات
            } else {
              showNotification(
                `❌ فشل حفظ طريقة الدفع: ${result.message}`,
                "error",
              );
            }
          })
          .catch((e) => console.error("❌ فشل حفظ طريقة الدفع:", e));
      }

      async function markAsDeliveredComplete(orderId) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) {
          showNotification("❌ لم يتم العثور على الطلب", "error");
          return;
        }

        const personnelInput = document.getElementById(
          `personnel-name-${orderId}`,
        );
        if (personnelInput && personnelInput.value.trim()) {
          order.deliveryPersonnelName = personnelInput.value.trim();
          order.deliveryPersonnelUpdatedAt = new Date().toISOString();
          order.deliveryPersonnelUpdatedBy = currentUser
            ? currentUser.name
            : "الكاشير";
        } else {
          showNotification("❌ يرجى إدخال اسم الموصل أولاً", "warning");
          personnelInput.style.border = "2px solid red";
          personnelInput.focus();
          return;
        }

        const paymentSelect = document.getElementById(`payment-${orderId}`);
        if (paymentSelect && paymentSelect.value) {
          order.deliveryPaymentMethod = paymentSelect.value;
          order.deliveryPaymentUpdatedAt = new Date().toISOString();
          order.deliveryPaymentUpdatedBy = currentUser
            ? currentUser.name
            : "الكاشير";
        } else {
          showNotification("❌ يرجى اختيار طريقة الدفع", "warning");
          paymentSelect.style.border = "2px solid red";
          paymentSelect.focus();
          return;
        }

        order.status = "delivered";
        order.statusUpdatedAt = new Date().toISOString();
        order.statusUpdatedBy = currentUser ? currentUser.name : "الكاشير";
        order.deliveredAt = new Date().toISOString();

        try {
          const result = await DataManager.saveDeliveryOrders(deliveryOrders);
          if (result.success) {
            localStorage.setItem(
              "kafta_delivery_orders",
              JSON.stringify(deliveryOrders),
            );
            showNotification(`✅ تم تأكيد توصيل الطلب`, "success");
            await loadUserDeliveryData(); // إعادة تحميل البيانات
          } else {
            showNotification(`❌ فشل التحديث: ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ:", error);
          showNotification("❌ حدث خطأ", "error");
        }
      }

      // دالة حفظ طريقة الدفع بشكل مباشر مع تحديث الواجهة
      async function savePaymentMethodDirect(orderId, paymentMethod) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) {
          showNotification("❌ لم يتم العثور على الطلب", "error");
          return;
        }

        // تحديث البيانات محلياً
        order.deliveryPaymentMethod = paymentMethod;
        order.deliveryPaymentUpdatedAt = new Date().toISOString();
        order.deliveryPaymentUpdatedBy = currentUser
          ? currentUser.name
          : "الكاشير";

        try {
          // حفظ في localStorage و Firebase إذا كان متصلاً
          localStorage.setItem(
            "kafta_delivery_orders",
            JSON.stringify(deliveryOrders),
          );

          if (navigator.onLine) {
            const result = await DataManager.saveDeliveryOrders(deliveryOrders);
            if (!result.success) {
              throw new Error(result.message);
            }
          } else {
            // إضافة للعمليات المعلقة للمزامنة لاحقاً
            SyncManager.addPendingOperation("delivery", order);
          }

          // تحديث واجهة المستخدم (إعادة تحميل القائمة مع الحفاظ على الفلترة)
          loadUserDeliveryOrders();

          // عرض رسالة نجاح مع اسم طريقة الدفع المختارة
          const methodName = getDeliveryPaymentMethodName(paymentMethod);
          showNotification(`✅ تم حفظ طريقة الدفع: ${methodName}`, "success");
        } catch (error) {
          console.error("❌ فشل حفظ طريقة الدفع:", error);
          showNotification("❌ حدث خطأ في حفظ طريقة الدفع", "error");
        }
      }

      async function updateDeliveryOrderStatus(orderId, newStatus) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) return;
        order.status = newStatus;
        order.statusUpdatedAt = new Date().toISOString();
        order.statusUpdatedBy = currentUser.name;
        if (newStatus === "delivered")
          order.deliveredAt = new Date().toISOString();
        // حفظ التغييرات
        localStorage.setItem(
          "kafta_delivery_orders",
          JSON.stringify(deliveryOrders),
        );
        if (navigator.onLine)
          await DataManager.saveDeliveryOrders(deliveryOrders);
        showNotification("✅ تم تحديث الحالة", "success");
      }

      async function updateDeliveryOrderComplete(orderId) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) {
          showNotification("❌ لم يتم العثور على الطلب", "error");
          return;
        }

        const personnelInput = document.getElementById(
          `personnel-name-${orderId}`,
        );
        if (personnelInput && personnelInput.value.trim()) {
          order.deliveryPersonnelName = personnelInput.value.trim();
          order.deliveryPersonnelUpdatedAt = new Date().toISOString();
          order.deliveryPersonnelUpdatedBy = currentUser
            ? currentUser.name
            : "الكاشير";
        }

        const paymentSelect = document.getElementById(`payment-${orderId}`);
        if (paymentSelect && paymentSelect.value) {
          order.deliveryPaymentMethod = paymentSelect.value;
          order.deliveryPaymentUpdatedAt = new Date().toISOString();
          order.deliveryPaymentUpdatedBy = currentUser
            ? currentUser.name
            : "الكاشير";
        }

        const statusSelect = document.getElementById(`status-${orderId}`);
        if (statusSelect && statusSelect.value) {
          const newStatus = statusSelect.value;
          if (newStatus !== order.status) {
            order.status = newStatus;
            order.statusUpdatedAt = new Date().toISOString();
            order.statusUpdatedBy = currentUser ? currentUser.name : "الكاشير";
            if (newStatus === "delivered")
              order.deliveredAt = new Date().toISOString();
          }
        }

        try {
          const result = await DataManager.saveDeliveryOrders(deliveryOrders);
          if (result.success) {
            localStorage.setItem(
              "kafta_delivery_orders",
              JSON.stringify(deliveryOrders),
            );
            showNotification(`✅ تم تحديث بيانات التوصيل بنجاح`, "success");
            await loadUserDeliveryData(); // إعادة تحميل البيانات
          } else {
            showNotification(`❌ فشل التحديث: ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في التحديث:", error);
          showNotification("❌ حدث خطأ في التحديث", "error");
        }
      }

      // ==================== دوال طباعة وتصدير الدليفري ====================
      function printAllDeliveryOrders() {
        const startDate = document.getElementById(
          "userDeliveryStartDate",
        ).value;
        const endDate = document.getElementById("userDeliveryEndDate").value;

        let filteredOrders = [...deliveryOrders];

        if (startDate && endDate) {
          const start = new Date(startDate);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDate);
          end.setHours(23, 59, 59, 999);

          filteredOrders = filteredOrders.filter((order) => {
            const orderDate = new Date(order.date);
            return orderDate >= start && orderDate <= end;
          });
        }

        if (filteredOrders.length === 0) {
          showNotification("❌ لا توجد طلبات للطباعة", "error");
          return;
        }

        // تحديث أسماء الموصلين من حقول الإدخال قبل الطباعة
        filteredOrders.forEach((order) => {
          const personnelInput = document.getElementById(
            `personnel-name-${order.id}`,
          );
          if (personnelInput && personnelInput.value.trim()) {
            order.deliveryPersonnelName = personnelInput.value.trim();
          }
        });

        localStorage.setItem(
          "kafta_delivery_orders",
          JSON.stringify(deliveryOrders),
        );

        const printWindow = window.open("", "", "width=800,height=600");
        const totalAmount = filteredOrders.reduce(
          (sum, o) => sum + (o.finalTotal || 0),
          0,
        );
        const deliveredCount = filteredOrders.filter(
          (o) => o.status === "delivered",
        ).length;
        const pendingCount = filteredOrders.filter(
          (o) => o.status === "pending" || o.status === "delivering",
        ).length;

        const html = `
    <!DOCTYPE html>
    <html dir="rtl">
    <head>
        <meta charset="UTF-8">
        <title>تقرير طلبات التوصيل</title>
        <style>
            body { font-family: Arial; padding: 30px; margin: 0; background: #fff; }
            .header { text-align: center; margin-bottom: 30px; border-bottom: 2px solid #333; padding-bottom: 20px; }
            .header h1 { color: #FF6B35; margin: 10px 0 5px; }
            .report-logo { width: 100px; height: 100px; border-radius: 50%; margin: 0 auto 15px; object-fit: cover; border: 3px solid #FFD700; }
            .summary { display: flex; justify-content: space-around; background: #f8f9fa; padding: 20px; border-radius: 10px; margin: 20px 0; }
            .summary-item { text-align: center; }
            .summary-value { font-size: 20px; font-weight: bold; color: #FF6B35; }
            table { width: 100%; border-collapse: collapse; margin: 25px 0; }
            th { background: #FF6B35; color: white; padding: 12px; }
            td { border: 1px solid #ddd; padding: 10px; text-align: center; }
            .status-pending { background: #FFC107; color: #000; padding: 5px 10px; border-radius: 20px; }
            .status-delivered { background: #4CAF50; color: white; padding: 5px 10px; border-radius: 20px; }
            .personnel-name { background: #e3f2fd; padding: 5px 10px; border-radius: 20px; font-weight: bold; color: #0d47a1; }
            .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
            .signature-box { width: 45%; text-align: center; border-top: 2px solid #333; padding-top: 15px; }
            .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 11px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
        </style>
    </head>
    <body>
        <div class="watermark">amaryasser408@gmail.com</div>
        <div class="header">
            <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
            <h1>🍖 ${restaurantInfo.name}</h1>
            <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
        </div>
        
        <h2 style="text-align: center; color: #FF6B35;">📋 تقرير طلبات التوصيل</h2>
        
        <div style="text-align: center; margin-bottom: 20px; padding: 15px; background: #e3f2fd; border-radius: 8px;">
            <p><strong>المستخدم:</strong> ${currentUser ? currentUser.name : "غير محدد"} | 
            <strong>الفترة:</strong> ${startDate || "البداية"} إلى ${endDate || "النهاية"}</p>
        </div>
        
        <div class="summary">
            <div class="summary-item"><div>📦 إجمالي الطلبات</div><div class="summary-value">${filteredOrders.length}</div></div>
            <div class="summary-item"><div>✅ تم التوصيل</div><div class="summary-value">${deliveredCount}</div></div>
            <div class="summary-item"><div>🔄 قيد التوصيل</div><div class="summary-value">${pendingCount}</div></div>
            <div class="summary-item"><div>💰 إجمالي المبيعات</div><div class="summary-value">${totalAmount.toFixed(2)} ج.م</div></div>
        </div>
        
        <table>
            <thead>
                <tr>
                    <th>رقم الفاتورة</th>
                    <th>التاريخ</th>
                    <th>العميل</th>
                    <th>مكان التوصيل</th>
                    <th>🚚 الموصل</th>
                    <th>💰 طريقة الدفع</th>
                    <th>الحالة</th>
                    <th>الإجمالي</th>
                </tr>
            </thead>
            <tbody>
                ${filteredOrders
                  .map((order) => {
                    const personnelName =
                      order.deliveryPersonnelName || "غير معين";
                    const paymentMethod =
                      getDeliveryPaymentMethodName(
                        order.deliveryPaymentMethod,
                      ) || "غير محدد";
                    const statusClass =
                      order.status === "delivered"
                        ? "status-delivered"
                        : "status-pending";
                    const statusName = getDeliveryStatusName(order.status);
                    // عرض المنطقة بدلاً من اسم العميل
                    const zoneDisplay = order.deliveryZone
                      ? `منطقة ${order.deliveryZone} (${order.deliveryPrice || 0} ج)`
                      : order.customerName || "-";
                    return `
                        <tr>
                            <td style="font-weight: bold;">${String(order.invoiceNumber).padStart(4, "0")}</td>
                            <td>${new Date(order.date).toLocaleDateString("en-GB")}</td>
                            <td>${zoneDisplay}</td>
                            <td>${order.deliveryLocation || "-"}</td>
                            <td><span class="personnel-name">${personnelName}</span></td>
                            <td>${paymentMethod}</td>
                            <td><span class="${statusClass}">${statusName}</span></td>
                            <td style="font-weight: bold; color: #FF6B35;">${(order.finalTotal || 0).toFixed(2)} ج.م</td>
                        </tr>
                    `;
                  })
                  .join("")}
            </tbody>
        </table>
        
        <div class="signature-section">
            <div class="signature-box"><p>الكاشير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
            <div class="signature-box"><p>المدير</p><p>....................</p></div>
        </div>
    </body>
    </html>
  `;

        printWindow.document.write(html);
        printWindow.document.close();
        setTimeout(() => printWindow.print(), 250);
        showNotification(
          `✅ تم تجهيز ${filteredOrders.length} طلب للطباعة`,
          "success",
        );
      }

      function exportUserDeliveryToExcel() {
        try {
          const startDate = document.getElementById(
            "userDeliveryStartDate",
          ).value;
          const endDate = document.getElementById("userDeliveryEndDate").value;

          let filteredOrders = [...deliveryOrders];

          if (startDate && endDate) {
            const start = new Date(startDate);
            start.setHours(0, 0, 0, 0);
            const end = new Date(endDate);
            end.setHours(23, 59, 59, 999);

            filteredOrders = filteredOrders.filter((order) => {
              const orderDate = new Date(order.date);
              return orderDate >= start && orderDate <= end;
            });
          }

          filteredOrders.forEach((order) => {
            const personnelInput = document.getElementById(
              `personnel-name-${order.id}`,
            );
            if (personnelInput && personnelInput.value.trim()) {
              order.deliveryPersonnelName = personnelInput.value.trim();
            }
          });

          const data = [];

          data.push(["تقرير طلبات التوصيل", "", "", "", "", "", "", ""]);
          data.push(["المطعم:", restaurantInfo.name, "", "", "", "", "", ""]);
          data.push([
            "الفرع:",
            `${restaurantInfo.number} - ${restaurantInfo.branchName}`,
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push(["الكاشير:", currentUser.name, "", "", "", "", "", ""]);
          data.push([
            "الفترة:",
            `${startDate || "البداية"} إلى ${endDate || "النهاية"}`,
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "تاريخ التصدير:",
            new Date().toLocaleDateString("ar-EG"),
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([]);

          data.push([
            "رقم الفاتورة",
            "التاريخ",
            "الوقت",
            "العميل",
            "مكان التوصيل",
            "رقم التوصيل",
            "🚚 الموصل",
            "💰 طريقة الدفع",
            "الحالة",
            "الإجمالي",
            "ملاحظات",
          ]);

          filteredOrders.forEach((order) => {
            data.push([
              String(order.invoiceNumber).padStart(4, "0"),
              new Date(order.date).toLocaleDateString("en-GB"),
              new Date(order.date).toLocaleTimeString("en-US", {
                hour: "2-digit",
                minute: "2-digit",
              }),
              order.customerName || "-",
              order.deliveryLocation || "-",
              order.deliveryNumber || "-",
              order.deliveryPersonnelName || "غير معين",
              getDeliveryPaymentMethodName(order.deliveryPaymentMethod) ||
                "غير محدد",
              getDeliveryStatusName(order.status),
              (order.finalTotal || 0).toFixed(2),
              order.orderNotes || "-",
            ]);
          });

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "طلبات_التوصيل");

          const wscols = [
            { wch: 12 },
            { wch: 12 },
            { wch: 10 },
            { wch: 20 },
            { wch: 25 },
            { wch: 15 },
            { wch: 20 },
            { wch: 15 },
            { wch: 15 },
            { wch: 15 },
            { wch: 30 },
          ];
          ws["!cols"] = wscols;

          const today = new Date().toISOString().split("T")[0];
          XLSX.writeFile(wb, `طلبات_التوصيل_${today}.xlsx`);

          showNotification("✅ تم تصدير التقرير بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification(
            "❌ حدث خطأ أثناء التصدير: " + error.message,
            "error",
          );
        }
      }

      // ==================== دوال تقرير نهاية الدوام ====================
      function printEndOfShiftReport() {
        const today = new Date();
        today.setHours(0, 0, 0, 0);
        const tomorrow = new Date(today);
        tomorrow.setDate(tomorrow.getDate() + 1);

        const todaySales = sales.filter((s) => {
          const saleDate = new Date(s.date);
          return saleDate >= today && saleDate < tomorrow;
        });

        const todayExpenses = expenses.filter((e) => {
          const expenseDate = new Date(e.date);
          return expenseDate >= today && expenseDate < tomorrow;
        });

        const totalSales = todaySales.reduce(
          (sum, s) => sum + (s.finalTotal || s.total),
          0,
        );
        const totalExpenses = todayExpenses.reduce(
          (sum, e) => sum + e.amount,
          0,
        );
        const netIncome = totalSales - totalExpenses;

        const printWindow = window.open("", "", "width=800,height=600");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head>
                <style>
                    body { font-family: Arial; padding: 20px; }
                    h2, h3 { text-align: center; }
                    .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                    table { width: 100%; border-collapse: collapse; margin: 10px 0; }
                    th, td { border: 1px solid #000; padding: 8px; text-align: center; }
                    .total { font-weight: bold; }
                    .expense { color: red; }
                    .customer-info { background-color: #f0f8ff; padding: 3px; }
                    .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 12px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
                    .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                    .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
                </style>
            </head>
            <body>
                <div class="watermark">amaryasser408@gmail.com</div>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                </div>
                <h3>تقرير نهاية الدوام - ${new Date().toLocaleDateString("en-GB")}</h3>
                <h4>المستخدم: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                <hr>
                <h4>ملخص اليوم:</h4>
                <table>
                    <tr><td>إجمالي المبيعات:</td><td class="total">${totalSales.toFixed(2)} جنيه</td></tr>
                    <tr><td>إجمالي المصاريف:</td><td class="total">${totalExpenses.toFixed(2)} جنيه</td></tr>
                    <tr><td>صافي الدخل:</td><td class="total">${netIncome.toFixed(2)} جنيه</td></tr>
                    <tr><td>عدد الطلبات:</td><td class="total">${todaySales.length}</td></tr>
                </table>
                <hr>
                <h4>الفواتير:</h4>
                <table>
                    <thead>
                        <tr>
                            <th>رقم الفاتورة</th><th>الوقت</th><th>نوع الطلب</th><th>العميل</th>
                            <th>رقم التوصيل</th><th>طريقة الدفع</th><th>الإجمالي</th><th>الخصم</th><th>الإجمالي النهائي</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${todaySales
                          .map(
                            (sale) => `
                            <tr>
                                <td>${String(sale.invoiceNumber).padStart(4, "0")}</td>
                                <td>${new Date(sale.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                                <td>${getOrderTypeName(sale.orderType)}</td>
                                <td class="customer-info">${sale.customerName || "-"}</td>
                                <td class="customer-info">${sale.deliveryNumber || "-"}</td>
                                <td>${getPaymentMethodName(sale.paymentMethod)}</td>
                                <td>${sale.total.toFixed(2)}</td>
                                <td>${(sale.discount || 0).toFixed(2)}</td>
                                <td>${(sale.finalTotal || sale.total).toFixed(2)}</td>
                            </tr>
                        `,
                          )
                          .join("")}
                    </tbody>
                </table>
                <h4>المصاريف:</h4>
                <table>
                    <thead>
                        <tr><th>الوقت</th><th>المبلغ</th><th>الوصف</th></tr>
                    </thead>
                    <tbody>
                        ${todayExpenses
                          .map(
                            (expense) => `
                            <tr class="expense">
                                <td>${new Date(expense.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                                <td>${expense.amount.toFixed(2)}</td>
                                <td>${expense.description}</td>
                            </tr>
                        `,
                          )
                          .join("")}
                    </tbody>
                </table>
                <div class="signature-section">
                    <div class="signature-box"><p>الكاشير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                    <div class="signature-box"><p>المدير</p><p>....................</p></div>
                </div>
            </body>
            </html>
        `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      function getOrderTypeName(type) {
        const types = { hall: "صالة", takeout: "تيك أوت", delivery: "توصيل" };
        return types[type] || type;
      }

      function getPaymentMethodName(method) {
        const methods = {
          cash: "كاش",
          bank: "بنكك",
          foori: "فوري",
          okash: "أوكاش",
          sahel: "ساهل",
        };
        return methods[method] || method;
      }

      // ==================== دوال المدير ====================
      async function loadAdminData() {
        try {
          products = await DataManager.getProducts();
          sales = await DataManager.getSales();
          expenses = await DataManager.getExpenses();
          orders = await DataManager.getOrders();
          categories = await DataManager.getCategories();
          employees = await DataManager.getEmployees();
          restaurantInfo = await DataManager.getRestaurantInfo();
          currentInvoiceNumber = await DataManager.getInvoiceNumber();

          users = await DataManager.getUsers();
          window.users = users;

          setTimeout(() => updateUserFilterOptions(), 100);
          initializeYearFilter();

          updateDashboard();
          loadAdminProducts();
          loadAdminSales();
          loadExpenses();
          loadCategories();
          loadEmployees();
          loadUsers();
          loadRestaurantInfo();

          updateProductCategorySelect();
          updateCategoryFilterOptions("admin");

          updateTime();
          setInterval(updateTime, 1000);
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات المدير:", error);
          showNotification("❌ حدث خطأ في تحميل البيانات", "error");
        }
        // تهيئة حقول التاريخ في شاشة المدير
        function initializeAdminDateFilters() {
          // الحصول على تاريخ اليوم بصيغة YYYY-MM-DD
          const today = new Date().toISOString().split("T")[0];

          // جلب جميع حقول التاريخ من الصفحة
          const salesStartDate = document.getElementById(
            "salesFilterStartDate",
          );
          const salesEndDate = document.getElementById("salesFilterEndDate");
          const expensesStartDate = document.getElementById(
            "expensesFilterStartDate",
          );
          const expensesEndDate = document.getElementById(
            "expensesFilterEndDate",
          );
          const productSalesStartDate = document.getElementById(
            "productSalesStartDate",
          );
          const productSalesEndDate = document.getElementById(
            "productSalesEndDate",
          );
          const adminDeliveryStartDate = document.getElementById(
            "adminDeliveryStartDate",
          );
          const adminDeliveryEndDate = document.getElementById(
            "adminDeliveryEndDate",
          );

          // تعيين قيمة تاريخ اليوم لكل حقل (إذا كان موجوداً)
          if (salesStartDate) salesStartDate.value = today;
          if (salesEndDate) salesEndDate.value = today;
          if (expensesStartDate) expensesStartDate.value = today;
          if (expensesEndDate) expensesEndDate.value = today;
          if (productSalesStartDate) productSalesStartDate.value = today;
          if (productSalesEndDate) productSalesEndDate.value = today;
          if (adminDeliveryStartDate) adminDeliveryStartDate.value = today;
          if (adminDeliveryEndDate) adminDeliveryEndDate.value = today;
        }
      }

      function updateDashboard() {
        const today = new Date();
        today.setHours(0, 0, 0, 0);
        const yesterday = new Date(today);
        yesterday.setDate(yesterday.getDate() - 1);

        const todaySales = sales.filter((s) => {
          const saleDate = new Date(s.date);
          saleDate.setHours(0, 0, 0, 0);
          return saleDate.getTime() === today.getTime();
        });

        const todayTotal = todaySales.reduce(
          (sum, s) => sum + (s.finalTotal || s.total),
          0,
        );

        const todayExpenses = expenses.filter((e) => {
          const expenseDate = new Date(e.date);
          expenseDate.setHours(0, 0, 0, 0);
          return expenseDate.getTime() === today.getTime();
        });

        const todayExpensesTotal = todayExpenses.reduce(
          (sum, e) => sum + e.amount,
          0,
        );

        document.getElementById("dashboardTotalSales").textContent =
          todayTotal.toFixed(2) + " جنيه";
        document.getElementById("dashboardTotalOrders").textContent =
          todaySales.length;
        document.getElementById("dashboardTotalProducts").textContent =
          products.length;
        document.getElementById("dashboardTotalExpenses").textContent =
          todayExpensesTotal.toFixed(2) + " جنيه";
      }

      // ==================== دوال إدارة المنتجات ====================
      async function loadAdminProducts() {
        const tbody = document.getElementById("productsTableBody");

        if (products.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="6" style="text-align: center;">لا توجد منتجات</td></tr>';
          return;
        }

        tbody.innerHTML = products
          .map((product) => {
            const price = product.price || 0;
            const ingredientsList =
              product.manualIngredients?.length > 0
                ? product.manualIngredients
                    .map(
                      (ing) => `${ing.name}: ${ing.quantity} ${ing.unit || ""}`,
                    )
                    .join(", ")
                : "لا يوجد مكونات";

            return `
                <tr>
                    <td><img src="${product.image}" alt="${product.name}" class="product-img" onerror="this.src='https://via.placeholder.com/50'"></td>
                    <td>${product.name}</td>
                    <td>${price.toFixed(2)} جنيه</td>
                    <td>${getCategoryName(product.category)}</td>
                    <td style="max-width: 200px; overflow: hidden; text-overflow: ellipsis;" title="${ingredientsList}">${ingredientsList}</td>
                    <td>
                        <div class="action-btns">
                            <button class="edit-btn" onclick="editProduct('${product.id}')"><i class="fas fa-edit"></i> تعديل</button>
                            <button class="delete-btn" onclick="deleteProduct('${product.id}')"><i class="fas fa-trash"></i> حذف</button>
                        </div>
                    </td>
                </tr>
            `;
          })
          .join("");

        const categorySelect = document.getElementById("productCategory");
        if (categorySelect) {
          categorySelect.innerHTML = categories
            .map(
              (category) =>
                `<option value="${category.id}">${category.name}</option>`,
            )
            .join("");
        }
      }

      function getCategoryName(categoryId) {
        if (!categoryId) return "غير محدد";
        const foundCategory = categories.find((c) => c.id === categoryId);
        return foundCategory ? foundCategory.name : categoryId;
      }

      async function addProduct() {
        const name = document.getElementById("productName").value.trim();
        const price = parseFloat(document.getElementById("productPrice").value);
        const category = document.getElementById("productCategory").value;
        const image = document.getElementById("productImage").value.trim();

        if (!name || !price || !category) {
          showNotification("❌ يرجى ملء جميع الحقول المطلوبة", "error");
          return;
        }

        if (currentProductManualIngredients.length === 0) {
          showNotification("❌ يرجى إضافة مكون واحد على الأقل للمنتج", "error");
          return;
        }

        try {
          if (editingProductId) {
            const productIndex = products.findIndex(
              (p) => p.id === editingProductId,
            );
            if (productIndex > -1) {
              const updatedProduct = {
                id: editingProductId,
                name: name,
                price: price,
                category: category,
                image: image || "https://via.placeholder.com/150",
                manualIngredients: [...currentProductManualIngredients],
                updatedAt: new Date().toISOString(),
              };

              products[productIndex] = updatedProduct;
              const result = await DataManager.saveProducts(products);

              if (result.success) {
                showNotification("✅ تم تحديث المنتج بنجاح", "success");
                editingProductId = null;
                const saveBtn = document.querySelector(
                  "#productsTab .btn-success",
                );
                if (saveBtn)
                  saveBtn.innerHTML =
                    '<i class="fas fa-plus"></i> إضافة المنتج';
              } else {
                showNotification(`❌ ${result.message}`, "error");
              }
            }
          } else {
            const newId = "prod_" + Date.now();
            const newProduct = {
              id: newId,
              name: name,
              price: price,
              category: category,
              image: image || "https://via.placeholder.com/150",
              manualIngredients: [...currentProductManualIngredients],
              createdAt: new Date().toISOString(),
            };

            products.push(newProduct);
            const result = await DataManager.saveProducts(products);

            if (result.success) {
              showNotification("✅ تم إضافة المنتج بنجاح", "success");
            } else {
              showNotification(`❌ ${result.message}`, "error");
            }
          }

          resetProductForm();
          loadAdminProducts();
          if (typeof displayProducts === "function") displayProducts("all");
        } catch (error) {
          console.error("❌ خطأ في حفظ المنتج:", error);
          showNotification("❌ حدث خطأ في حفظ المنتج", "error");
        }
      }

      function editProduct(id) {
        const product = products.find((p) => p.id === id);
        if (!product) {
          showNotification("❌ المنتج غير موجود", "error");
          return;
        }

        editingProductId = id;
        document.getElementById("productName").value = product.name;
        document.getElementById("productPrice").value = product.price;
        document.getElementById("productCategory").value = product.category;
        document.getElementById("productImage").value = product.image || "";

        currentProductManualIngredients = product.manualIngredients
          ? [...product.manualIngredients]
          : [];
        updateProductManualIngredientsList();

        document.querySelector("#productsTab .btn-success").innerHTML =
          '<i class="fas fa-save"></i> تحديث المنتج';
        showNotification(`📝 تعديل المنتج: ${product.name}`, "info");
        document
          .getElementById("productsTab")
          .scrollIntoView({ behavior: "smooth" });
      }

      async function deleteProduct(id) {
        if (!confirm("هل أنت متأكد من حذف هذا المنتج؟")) return;

        try {
          products = products.filter((p) => p.id !== id);
          const result = await DataManager.saveProducts(products);

          if (result.success) {
            showNotification("✅ تم حذف المنتج بنجاح", "success");
            loadAdminProducts();
            if (typeof displayProducts === "function") displayProducts("all");
          } else {
            showNotification("❌ فشل الحذف: " + result.message, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في حذف المنتج:", error);
          showNotification("❌ حدث خطأ أثناء حذف المنتج", "error");
        }
      }

      function resetProductForm() {
        document.getElementById("productName").value = "";
        document.getElementById("productPrice").value = "";
        document.getElementById("productCategory").value = "";
        document.getElementById("productImage").value = "";

        currentProductManualIngredients = [];
        updateProductManualIngredientsList();

        document.querySelector("#productsTab .btn-success").innerHTML =
          '<i class="fas fa-plus"></i> إضافة المنتج';
        editingProductId = null;
      }

      // ==================== دوال المكونات اليدوية ====================
      function addManualIngredient() {
        const name = document
          .getElementById("manualIngredientName")
          .value.trim();
        const quantity = document
          .getElementById("manualIngredientQuantity")
          .value.trim();
        const unit = document.getElementById("manualIngredientUnit").value;

        if (!name || !quantity) {
          showNotification("❌ يرجى إدخال اسم المكون والكمية", "error");
          return;
        }

        const existingIndex = currentProductManualIngredients.findIndex(
          (ing) => ing.name === name,
        );

        if (existingIndex >= 0) {
          currentProductManualIngredients[existingIndex].quantity = quantity;
          currentProductManualIngredients[existingIndex].unit = unit;
        } else {
          currentProductManualIngredients.push({
            name: name,
            quantity: quantity,
            unit: unit,
          });
        }

        document.getElementById("manualIngredientName").value = "";
        document.getElementById("manualIngredientQuantity").value = "";
        document.getElementById("manualIngredientUnit").value = "قطعة";

        updateProductManualIngredientsList();
      }

      function updateProductManualIngredientsList() {
        const container = document.getElementById(
          "productIngredientsManualList",
        );

        if (currentProductManualIngredients.length === 0) {
          container.innerHTML =
            '<div class="empty-state"><div class="empty-state-icon"><i class="fas fa-carrot"></i></div><p>لم تضف أي مكونات بعد</p></div>';
          return;
        }

        container.innerHTML = currentProductManualIngredients
          .map(
            (ingredient, index) => `
            <div class="product-ingredient-manual-item">
                <div class="product-ingredient-manual-name">${ingredient.name}</div>
                <div class="product-ingredient-manual-quantity">${ingredient.quantity} ${ingredient.unit || ""}</div>
                <button class="invoice-item-remove" onclick="removeManualIngredient(${index})"><i class="fas fa-times"></i></button>
            </div>
        `,
          )
          .join("");
      }

      function removeManualIngredient(index) {
        currentProductManualIngredients.splice(index, 1);
        updateProductManualIngredientsList();
      }

      // ==================== دوال إدارة الدليفري للمدير ====================
      async function loadAdminDeliveryData() {
        try {
          // محاولة التحميل من Firebase أولاً إذا كان متصلاً
          if (navigator.onLine) {
            const firebaseOrders = await DataManager.getDeliveryOrders();
            if (firebaseOrders && firebaseOrders.length > 0) {
              deliveryOrders = firebaseOrders;
              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
            } else {
              // إذا كانت Firebase فارغة، استخدم localStorage
              const saved = localStorage.getItem("kafta_delivery_orders");
              deliveryOrders = saved ? JSON.parse(saved) : [];
            }
          } else {
            // إذا كان غير متصل، استخدم localStorage
            const saved = localStorage.getItem("kafta_delivery_orders");
            deliveryOrders = saved ? JSON.parse(saved) : [];
          }

          console.log(
            "📦 deliveryOrders after load:",
            deliveryOrders.length,
            deliveryOrders,
          );

          // تعيين التواريخ الافتراضية
          const today = new Date().toISOString().split("T")[0];
          const startDateInput = document.getElementById(
            "adminDeliveryStartDate",
          );
          const endDateInput = document.getElementById("adminDeliveryEndDate");
          if (startDateInput) startDateInput.value = today;
          if (endDateInput) endDateInput.value = today;

          updateAdminDeliveryCashierSelect();
          loadAdminDeliveryOrders(); // ستعيد تطبيق الفلترة باستخدام deliveryOrders الحالية
          updateAdminDeliveryStats();

          if (deliveryOrders.length === 0) {
            showNotification(
              "⚠️ لا توجد طلبات توصيل في قاعدة البيانات",
              "warning",
            );
          } else {
            showNotification(
              `✅ تم تحميل ${deliveryOrders.length} طلب توصيل`,
              "success",
            );
          }

          console.log(
            "✅ تم تحميل بيانات الدليفري للمدير بنجاح، عدد الطلبات:",
            deliveryOrders.length,
          );
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات الدليفري للمدير:", error);
          showNotification("❌ حدث خطأ في تحميل البيانات", "error");
        }
      }

      function updateAdminDeliveryCashierSelect() {
        const cashierSelect = document.getElementById("adminDeliveryCashier");
        if (!cashierSelect) return;

        cashierSelect.innerHTML = '<option value="all">جميع الكاشيرات</option>';

        const cashiers = [
          ...new Set(
            deliveryOrders.map((order) => order.cashier).filter(Boolean),
          ),
        ];
        cashiers.forEach((cashier) => {
          const option = document.createElement("option");
          option.value = cashier;
          option.textContent = cashier;
          cashierSelect.appendChild(option);
        });
      }

      function updateAdminDeliveryStats() {
        const today = new Date();
        today.setHours(0, 0, 0, 0);
        const tomorrow = new Date(today);
        tomorrow.setDate(tomorrow.getDate() + 1);

        // طلبات اليوم
        const todaysOrders = deliveryOrders.filter((order) => {
          const orderDate = new Date(order.date);
          return orderDate >= today && orderDate < tomorrow;
        });

        // إجمالي جميع الطلبات (وليس فقط اليوم)
        const totalOrders = deliveryOrders.length;
        const pendingOrders = deliveryOrders.filter(
          (o) => o.status === "pending" || o.status === "delivering",
        ).length;
        const deliveredOrders = deliveryOrders.filter(
          (o) => o.status === "delivered",
        ).length;
        const totalSales = deliveryOrders.reduce(
          (sum, o) => sum + (o.finalTotal || 0),
          0,
        );

        // تحديث العناصر في الواجهة
        document.getElementById("adminTotalDeliveryOrders").textContent =
          totalOrders;
        document.getElementById("adminPendingDelivery").textContent =
          pendingOrders;
        document.getElementById("adminDeliveredOrders").textContent =
          deliveredOrders;
        document.getElementById("adminTotalDeliverySales").textContent =
          totalSales.toFixed(2) + " جنيه";

        console.log("📊 إحصائيات الدليفري:", {
          totalOrders,
          pendingOrders,
          deliveredOrders,
          totalSales,
        });
      }

      function loadAdminDeliveryOrders() {
        const startDateInput = document.getElementById(
          "adminDeliveryStartDate",
        );
        const endDateInput = document.getElementById("adminDeliveryEndDate");
        const statusSelect = document.getElementById("adminDeliveryStatus");
        const paymentMethodSelect = document.getElementById(
          "deliveryPaymentMethod",
        );
        const personnelNameInput = document.getElementById(
          "adminDeliveryPersonnelName",
        );
        const cashierSelect = document.getElementById("adminDeliveryCashier");

        const startDate = startDateInput ? startDateInput.value : "";
        const endDate = endDateInput ? endDateInput.value : "";
        const status = statusSelect ? statusSelect.value : "all";
        const paymentMethod = paymentMethodSelect
          ? paymentMethodSelect.value
          : "all";
        const personnelName = personnelNameInput
          ? personnelNameInput.value.trim()
          : "";
        const cashier = cashierSelect ? cashierSelect.value : "all";

        let filteredOrders = [...deliveryOrders];

        // فلترة حسب التاريخ
        if (startDate && endDate) {
          const start = new Date(startDate);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDate);
          end.setHours(23, 59, 59, 999);

          filteredOrders = filteredOrders.filter((order) => {
            const orderDate = new Date(order.date);
            return orderDate >= start && orderDate <= end;
          });
        }

        // فلترة حسب الحالة
        if (status !== "all") {
          filteredOrders = filteredOrders.filter(
            (order) => order.status === status,
          );
        }

        // فلترة حسب طريقة الدفع
        if (paymentMethod !== "all") {
          filteredOrders = filteredOrders.filter(
            (order) => order.deliveryPaymentMethod === paymentMethod,
          );
        }

        // فلترة حسب اسم الموصل
        if (personnelName) {
          filteredOrders = filteredOrders.filter((order) =>
            order.deliveryPersonnelName
              ?.toLowerCase()
              .includes(personnelName.toLowerCase()),
          );
        }

        // فلترة حسب الكاشير
        if (cashier !== "all") {
          filteredOrders = filteredOrders.filter(
            (order) => order.cashier === cashier,
          );
        }

        // ترتيب تنازلي حسب التاريخ
        filteredOrders.sort((a, b) => new Date(b.date) - new Date(a.date));

        displayAdminDeliveryOrders(filteredOrders);

        // ✅ تحديث الإحصائيات بالطلبات المفلترة
        const totalOrdersFiltered = filteredOrders.length;
        const pendingFiltered = filteredOrders.filter(
          (o) => o.status === "pending" || o.status === "delivering",
        ).length;
        const deliveredFiltered = filteredOrders.filter(
          (o) => o.status === "delivered",
        ).length;
        const totalSalesFiltered = filteredOrders.reduce(
          (sum, o) => sum + (o.finalTotal || 0),
          0,
        );

        document.getElementById("adminTotalDeliveryOrders").textContent =
          totalOrdersFiltered;
        document.getElementById("adminPendingDelivery").textContent =
          pendingFiltered;
        document.getElementById("adminDeliveredOrders").textContent =
          deliveredFiltered;
        document.getElementById("adminTotalDeliverySales").textContent =
          totalSalesFiltered.toFixed(2) + " جنيه";

        const countElement = document.getElementById("adminDeliveryCount");
        if (countElement)
          countElement.textContent = `${filteredOrders.length} طلب`;

        console.log("🔍 filteredOrders:", filteredOrders.length);
      }

      async function loadAdminDeliveryData() {
        try {
          // محاولة التحميل من Firebase أولاً إذا كان متصلاً
          if (navigator.onLine) {
            const firebaseOrders = await DataManager.getDeliveryOrders();
            if (firebaseOrders && firebaseOrders.length > 0) {
              deliveryOrders = firebaseOrders;
              localStorage.setItem(
                "kafta_delivery_orders",
                JSON.stringify(deliveryOrders),
              );
            } else {
              // إذا كانت Firebase فارغة، استخدم localStorage
              const saved = localStorage.getItem("kafta_delivery_orders");
              deliveryOrders = saved ? JSON.parse(saved) : [];
            }
          } else {
            // إذا كان غير متصل، استخدم localStorage
            const saved = localStorage.getItem("kafta_delivery_orders");
            deliveryOrders = saved ? JSON.parse(saved) : [];
          }

          console.log(
            "📦 deliveryOrders after load:",
            deliveryOrders.length,
            deliveryOrders,
          );

          // تعيين التواريخ الافتراضية
          const today = new Date().toISOString().split("T")[0];
          const startDateInput = document.getElementById(
            "adminDeliveryStartDate",
          );
          const endDateInput = document.getElementById("adminDeliveryEndDate");
          if (startDateInput) startDateInput.value = today;
          if (endDateInput) endDateInput.value = today;

          updateAdminDeliveryCashierSelect();
          loadAdminDeliveryOrders(); // ستعيد تطبيق الفلترة باستخدام deliveryOrders الحالية
          updateAdminDeliveryStats();

          if (deliveryOrders.length === 0) {
            showNotification(
              "⚠️ لا توجد طلبات توصيل في قاعدة البيانات",
              "warning",
            );
          } else {
            showNotification(
              `✅ تم تحميل ${deliveryOrders.length} طلب توصيل`,
              "success",
            );
          }

          console.log(
            "✅ تم تحميل بيانات الدليفري للمدير بنجاح، عدد الطلبات:",
            deliveryOrders.length,
          );
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات الدليفري للمدير:", error);
          showNotification("❌ حدث خطأ في تحميل البيانات", "error");
        }
      }

      function displayAdminDeliveryOrders(orders) {
        const tbody = document.getElementById("adminDeliveryOrdersTableBody");

        if (orders.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="12" style="text-align: center;">لا توجد بيانات</td></tr>';
          return;
        }

        tbody.innerHTML = orders
          .map((order) => {
            const statusClass = getDeliveryStatusClass(order.status);
            const statusName = getDeliveryStatusName(order.status);

            return `
                <tr>
                    <td style="font-weight: bold;">${String(order.invoiceNumber).padStart(4, "0")}</td>
                    <td>${new Date(order.date).toLocaleDateString("en-GB")}</td>
                    <td>${new Date(order.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                    <td>${order.customerName || "-"}</td>
                    <td style="max-width: 200px; white-space: normal;">${order.deliveryLocation || "-"}</td>
                    <td>${order.deliveryNumber || "-"}</td>
                    <td><span style="background: #e3f2fd; padding: 5px 10px; border-radius: 20px; font-weight: bold; color: #0d47a1;">${order.deliveryPersonnelName || "غير معين"}</span></td>
                    <td><span style="background: ${getPaymentMethodColor(order.deliveryPaymentMethod)}; padding: 5px 10px; border-radius: 20px; color: white; font-weight: bold;">${getDeliveryPaymentMethodName(order.deliveryPaymentMethod)}</span></td>
                    <td><span class="delivery-order-status ${statusClass}" style="padding: 5px 10px; border-radius: 20px;">${statusName}</span></td>
                    <td style="font-weight: bold; color: var(--secondary-color);">${(order.finalTotal || 0).toFixed(2)} جنيه</td>
                    <td>${order.cashier || "-"}</td>
                    <td>
                        <div style="display: flex; gap: 5px; align-items: center;">
                            <button class="btn btn-print" onclick="printSingleDeliveryInvoice('${order.id}')" title="طباعة الفاتورة" style="padding: 6px 12px; background: #607D8B; color: white; border: none; border-radius: 5px; cursor: pointer;">
                                <i class="fas fa-print"></i>
                            </button>
                            <button class="btn btn-info" onclick="viewDeliveryOrderDetails('${order.id}')" title="عرض التفاصيل" style="padding: 6px 12px; background: #2196F3; color: white; border: none; border-radius: 5px; cursor: pointer;">
                                <i class="fas fa-eye"></i>
                            </button>
                            <select id="admin-status-${order.id}" style="padding: 6px; border-radius: 5px; border: 1px solid #ddd; background: white;" onchange="updateDeliveryOrderFromAdmin('${order.id}')">
                                <option value="pending" ${order.status === "pending" ? "selected" : ""}>🟡 في انتظار التوصيل</option>
                                <option value="delivering" ${order.status === "delivering" ? "selected" : ""}>🔵 قيد التوصيل</option>
                                <option value="delivered" ${order.status === "delivered" ? "selected" : ""}>✅ تم التوصيل</option>
                                <option value="cancelled" ${order.status === "cancelled" ? "selected" : ""}>❌ ملغي</option>
                            </select>
                        </div>
                    </td>
                </tr>
            `;
          })
          .join("");
      }

      async function updateDeliveryOrderFromAdmin(orderId) {
        const statusSelect = document.getElementById(`admin-status-${orderId}`);
        const newStatus = statusSelect.value;

        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) return;

        if (newStatus !== order.status) {
          order.status = newStatus;
          order.statusUpdatedAt = new Date().toISOString();
          order.statusUpdatedBy = currentUser.name;

          if (newStatus === "delivered")
            order.deliveredAt = new Date().toISOString();

          try {
            localStorage.setItem(
              "kafta_delivery_orders",
              JSON.stringify(deliveryOrders),
            );
            await DataManager.saveDeliveryOrders(deliveryOrders);
            showNotification("✅ تم تحديث حالة الطلب بنجاح", "success");
            updateAdminDeliveryStats();
          } catch (error) {
            console.error("❌ خطأ في تحديث الطلب:", error);
            showNotification("❌ حدث خطأ في تحديث الطلب", "error");
          }
        }
      }
      function viewDeliveryOrderDetails(orderId) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) return;

        const personnelName = getPersonnelName(order.deliveryPersonnelId);
        const statusName = getDeliveryStatusName(order.status);

        const detailsHTML = `
            <div style="padding: 15px;">
                <h3 style="color: var(--secondary-color); border-bottom: 2px solid var(--primary-color); padding-bottom: 10px; margin-bottom: 15px;">
                    تفاصيل طلب التوصيل - فاتورة رقم ${String(order.invoiceNumber).padStart(4, "0")}
                </h3>
                
                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                    <div>
                        <h4>معلومات الطلب</h4>
                        <p><strong>التاريخ:</strong> ${new Date(order.date).toLocaleDateString("en-GB")}</p>
                        <p><strong>الوقت:</strong> ${new Date(order.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</p>
                        <p><strong>الكاشير:</strong> ${order.cashier || "-"}</p>
                        <p><strong>الحالة:</strong> <span style="color: ${getStatusColor(order.status)}; font-weight: bold;">${statusName}</span></p>
                    </div>
                    <div>
                        <h4>معلومات العميل</h4>
                        <p><strong>الاسم:</strong> ${order.customerName || "غير محدد"}</p>
                        <p><strong>رقم التوصيل:</strong> ${order.deliveryNumber || "غير محدد"}</p>
                        <p><strong>مكان التوصيل:</strong> ${order.deliveryLocation || "غير محدد"}</p>
                        <p><strong>الموصل:</strong> ${personnelName}</p>
                    </div>
                </div>
                
                <h4 style="margin-top: 20px;">المنتجات</h4>
                <table style="width: 100%; border-collapse: collapse; margin-top: 10px;">
                    <thead>
                        <tr style="background: #f5f5f5;">
                            <th style="border: 1px solid #ddd; padding: 8px;">المنتج</th>
                            <th style="border: 1px solid #ddd; padding: 8px;">الكمية</th>
                            <th style="border: 1px solid #ddd; padding: 8px;">السعر</th>
                            <th style="border: 1px solid #ddd; padding: 8px;">الإجمالي</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${order.items
                          .map(
                            (item) => `
                            <tr>
                                <td style="border: 1px solid #ddd; padding: 8px;">${item.name}</td>
                                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${item.quantity}</td>
                                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${(item.price || 0).toFixed(2)}</td>
                                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${((item.price || 0) * item.quantity).toFixed(2)}</td>
                            </tr>
                        `,
                          )
                          .join("")}
                    </tbody>
                    <tfoot>
                        <tr>
                            <td colspan="3" style="border: 1px solid #ddd; padding: 10px; text-align: left; font-weight: bold;">الإجمالي الكلي:</td>
                            <td style="border: 1px solid #ddd; padding: 10px; text-align: center; font-weight: bold; color: var(--secondary-color);">
                                ${(order.finalTotal || 0).toFixed(2)} جنيه
                            </td>
                        </tr>
                    </tfoot>
                </table>
                
                ${
                  order.orderNotes
                    ? `
                    <div style="margin-top: 15px; padding: 10px; background: #fff3cd; border-radius: 5px;">
                        <strong>ملاحظات:</strong> ${order.orderNotes}
                    </div>
                `
                    : ""
                }
                
                ${
                  order.deliveredAt
                    ? `
                    <div style="margin-top: 15px; padding: 10px; background: #e8f5e9; border-radius: 5px;">
                        <strong>تم التوصيل في:</strong> ${new Date(order.deliveredAt).toLocaleString("en-GB")}
                    </div>
                `
                    : ""
                }
            </div>
        `;

        const modal = document.createElement("div");
        modal.className = "quantity-modal-overlay";
        modal.style.display = "flex";
        modal.innerHTML = `
            <div class="quantity-modal" style="max-width: 800px; max-height: 80vh; overflow-y: auto;">
                <div class="quantity-modal-header">
                    <button class="quantity-modal-close" onclick="this.closest('.quantity-modal-overlay').remove()">
                        <i class="fas fa-times"></i>
                    </button>
                    <div class="quantity-modal-product">تفاصيل طلب التوصيل</div>
                </div>
                <div class="quantity-display" style="max-height: none; overflow-y: visible;">
                    ${detailsHTML}
                </div>
                <div class="quantity-keypad">
                    <div class="quantity-action-buttons">
                        <button class="quantity-action-btn quantity-cancel-btn" onclick="this.closest('.quantity-modal-overlay').remove()">
                            <i class="fas fa-times"></i> إغلاق
                        </button>
                        <button class="quantity-action-btn quantity-add-btn" onclick="printSingleDeliveryInvoice('${order.id}')">
                            <i class="fas fa-print"></i> طباعة الفاتورة
                        </button>
                    </div>
                </div>
            </div>
        `;
        document.body.appendChild(modal);
      }

      function printAdminDeliveryReport() {
        const startDateInput = document.getElementById(
          "adminDeliveryStartDate",
        );
        const endDateInput = document.getElementById("adminDeliveryEndDate");
        const statusSelect = document.getElementById("adminDeliveryStatus");
        const paymentMethodSelect = document.getElementById(
          "adminDeliveryPaymentMethod",
        );
        const personnelNameInput = document.getElementById(
          "adminDeliveryPersonnelName",
        );
        const cashierSelect = document.getElementById("adminDeliveryCashier");

        const startDate = startDateInput ? startDateInput.value : "";
        const endDate = endDateInput ? endDateInput.value : "";
        const status = statusSelect ? statusSelect.value : "all";
        const paymentMethod = paymentMethodSelect
          ? paymentMethodSelect.value
          : "all";
        const personnelName = personnelNameInput
          ? personnelNameInput.value.trim()
          : "";
        const cashier = cashierSelect ? cashierSelect.value : "all";

        let filteredOrders = [...deliveryOrders];

        if (startDate && endDate) {
          const start = new Date(startDate);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDate);
          end.setHours(23, 59, 59, 999);
          filteredOrders = filteredOrders.filter((o) => {
            const orderDate = new Date(o.date);
            return orderDate >= start && orderDate <= end;
          });
        }

        if (status !== "all")
          filteredOrders = filteredOrders.filter((o) => o.status === status);
        if (paymentMethod !== "all")
          filteredOrders = filteredOrders.filter(
            (o) => o.deliveryPaymentMethod === paymentMethod,
          );
        if (personnelName)
          filteredOrders = filteredOrders.filter((o) =>
            o.deliveryPersonnelName
              ?.toLowerCase()
              .includes(personnelName.toLowerCase()),
          );
        if (cashier !== "all")
          filteredOrders = filteredOrders.filter((o) => o.cashier === cashier);

        if (filteredOrders.length === 0) {
          showNotification("❌ لا توجد بيانات للطباعة", "error");
          return;
        }

        const totalAmount = filteredOrders.reduce(
          (sum, o) => sum + (o.finalTotal || 0),
          0,
        );
        const deliveredCount = filteredOrders.filter(
          (o) => o.status === "delivered",
        ).length;
        const pendingCount = filteredOrders.filter(
          (o) => o.status === "pending" || o.status === "delivering",
        ).length;

        const printWindow = window.open("", "", "width=1200,height=700");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head>
                <meta charset="UTF-8">
                <title>تقرير الدليفري - إدارة المطعم</title>
                <style>
                    body { font-family: Arial; padding: 20px; }
                    h2, h3 { text-align: center; }
                    .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; }
                    table { width: 100%; border-collapse: collapse; margin: 10px 0; font-size: 12px; }
                    th, td { border: 1px solid #000; padding: 6px; text-align: center; }
                    th { background: #f2f2f2; }
                    .summary { display: flex; justify-content: space-between; margin: 20px 0; padding: 15px; background: #f9f9f9; border-radius: 5px; }
                    .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                    .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
                    .filter-info { background: #e3f2fd; padding: 10px; border-radius: 5px; margin-bottom: 20px; }
                    .status-pending { background: #FFC107; color: black; padding: 3px 8px; border-radius: 15px; }
                    .status-delivering { background: #2196F3; color: white; padding: 3px 8px; border-radius: 15px; }
                    .status-delivered { background: #4CAF50; color: white; padding: 3px 8px; border-radius: 15px; }
                </style>
            </head>
            <body>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                </div>
                
                <h3>تقرير إدارة الدليفري</h3>
                <h4>المدير: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                <h4>تاريخ التقرير: ${new Date().toLocaleDateString("ar-EG")}</h4>
                
                <div class="filter-info">
                    <strong>معايير الفلترة:</strong><br>
                    الفترة: ${startDate || "البداية"} إلى ${endDate || "النهاية"} |
                    الحالة: ${status === "all" ? "جميع الحالات" : getDeliveryStatusName(status)} |
                    طريقة الدفع: ${paymentMethod === "all" ? "جميع الطرق" : getDeliveryPaymentMethodName(paymentMethod)} |
                    الموصل: ${personnelName || "جميع الموصلين"} |
                    الكاشير: ${cashier === "all" ? "جميع الكاشيرات" : cashier}
                </div>
                
                <div class="summary">
                    <div><strong>إجمالي الطلبات:</strong> ${filteredOrders.length}</div>
                    <div><strong>تم التوصيل:</strong> ${deliveredCount}</div>
                    <div><strong>قيد التوصيل:</strong> ${pendingCount}</div>
                    <div><strong>إجمالي المبيعات:</strong> ${totalAmount.toFixed(2)} جنيه</div>
                </div>
                
                <table>
                    <thead>
                        <tr>
                            <th>رقم الفاتورة</th><th>التاريخ</th><th>الوقت</th><th>العميل</th>
                            <th>مكان التوصيل</th><th>الموصل</th><th>طريقة الدفع</th><th>الحالة</th><th>الإجمالي</th><th>الكاشير</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${filteredOrders
                          .map(
                            (order) => `
                            <tr>
                                <td>${String(order.invoiceNumber).padStart(4, "0")}</td>
                                <td>${new Date(order.date).toLocaleDateString("en-GB")}</td>
                                <td>${new Date(order.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                                <td>${order.customerName || "-"}</td>
                                <td>${order.deliveryLocation || "-"}</td>
                                <td>${order.deliveryPersonnelName || "غير معين"}</td>
                                <td>${getDeliveryPaymentMethodName(order.deliveryPaymentMethod) || "غير محدد"}</td>
                                <td class="status-${order.status}">${getDeliveryStatusName(order.status)}</td>
                                <td>${(order.finalTotal || 0).toFixed(2)}</td>
                                <td>${order.cashier || "-"}</td>
                            </tr>
                        `,
                          )
                          .join("")}
                    </tbody>
                </table>
                
                <div class="signature-section">
                    <div class="signature-box"><p>المدير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                    <div class="signature-box"><p>ختم المطعم</p><p>....................</p></div>
                </div>
            </body>
            </html>
        `;

        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      function exportAdminDeliveryToExcel() {
        try {
          const startDateInput = document.getElementById(
            "adminDeliveryStartDate",
          );
          const endDateInput = document.getElementById("adminDeliveryEndDate");
          const statusSelect = document.getElementById("adminDeliveryStatus");
          const paymentMethodSelect = document.getElementById(
            "adminDeliveryPaymentMethod",
          );
          const personnelNameInput = document.getElementById(
            "adminDeliveryPersonnelName",
          );
          const cashierSelect = document.getElementById("adminDeliveryCashier");

          const startDate = startDateInput ? startDateInput.value : "";
          const endDate = endDateInput ? endDateInput.value : "";
          const status = statusSelect ? statusSelect.value : "all";
          const paymentMethod = paymentMethodSelect
            ? paymentMethodSelect.value
            : "all";
          const personnelName = personnelNameInput
            ? personnelNameInput.value.trim()
            : "";
          const cashier = cashierSelect ? cashierSelect.value : "all";

          let filteredOrders = [...deliveryOrders];

          if (startDate && endDate) {
            const start = new Date(startDate);
            start.setHours(0, 0, 0, 0);
            const end = new Date(endDate);
            end.setHours(23, 59, 59, 999);
            filteredOrders = filteredOrders.filter((o) => {
              const orderDate = new Date(o.date);
              return orderDate >= start && orderDate <= end;
            });
          }

          if (status !== "all")
            filteredOrders = filteredOrders.filter((o) => o.status === status);
          if (paymentMethod !== "all")
            filteredOrders = filteredOrders.filter(
              (o) => o.deliveryPaymentMethod === paymentMethod,
            );
          if (personnelName)
            filteredOrders = filteredOrders.filter((o) =>
              o.deliveryPersonnelName
                ?.toLowerCase()
                .includes(personnelName.toLowerCase()),
            );
          if (cashier !== "all")
            filteredOrders = filteredOrders.filter(
              (o) => o.cashier === cashier,
            );

          if (filteredOrders.length === 0) {
            showNotification("❌ لا توجد بيانات للتصدير", "error");
            return;
          }

          const data = [];

          data.push([
            "تقرير إدارة الدليفري",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "المطعم:",
            restaurantInfo.name,
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "الفرع:",
            `${restaurantInfo.number} - ${restaurantInfo.branchName}`,
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "المدير:",
            currentUser ? currentUser.name : "غير محدد",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "تاريخ التقرير:",
            new Date().toLocaleDateString("ar-EG"),
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "الفترة:",
            `${startDate || "البداية"} إلى ${endDate || "النهاية"}`,
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "الحالة:",
            status === "all" ? "جميع الحالات" : getDeliveryStatusName(status),
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "طريقة الدفع:",
            paymentMethod === "all"
              ? "جميع الطرق"
              : getDeliveryPaymentMethodName(paymentMethod),
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "الموصل:",
            personnelName || "جميع الموصلين",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "الكاشير:",
            cashier === "all" ? "جميع الكاشيرات" : cashier,
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
            "",
          ]);
          data.push([]);

          data.push([
            "رقم الفاتورة",
            "التاريخ",
            "الوقت",
            "العميل",
            "مكان التوصيل",
            "رقم التوصيل",
            "الموصل",
            "طريقة الدفع",
            "الحالة",
            "الإجمالي",
            "الكاشير",
            "ملاحظات",
          ]);

          filteredOrders.forEach((order) => {
            data.push([
              String(order.invoiceNumber).padStart(4, "0"),
              new Date(order.date).toLocaleDateString("en-GB"),
              new Date(order.date).toLocaleTimeString("en-US", {
                hour: "2-digit",
                minute: "2-digit",
              }),
              order.customerName || "-",
              order.deliveryLocation || "-",
              order.deliveryNumber || "-",
              order.deliveryPersonnelName || "غير معين",
              getDeliveryPaymentMethodName(order.deliveryPaymentMethod) ||
                "غير محدد",
              getDeliveryStatusName(order.status),
              (order.finalTotal || 0).toFixed(2),
              order.cashier || "-",
              order.orderNotes || "-",
            ]);
          });

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "إدارة_الدليفري");

          const today = new Date().toISOString().split("T")[0];
          XLSX.writeFile(wb, `تقرير_إدارة_الدليفري_${today}.xlsx`);

          showNotification("✅ تم تصدير التقرير بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification(
            "❌ حدث خطأ أثناء التصدير: " + error.message,
            "error",
          );
        }
      }

      // ==================== دوال المبيعات للمدير ====================
      async function loadAdminSales() {
        const startDateInput = document.getElementById("salesFilterStartDate");
        const endDateInput = document.getElementById("salesFilterEndDate");
        const user = document.getElementById("salesFilterUser").value;
        const categoryId = document.getElementById("salesFilterCategory").value;
        const paymentMethod =
          document.getElementById("salesPaymentMethod")?.value || "all"; // إضافة فلترة طريقة الدفع

        let filteredSales = [...sales];

        if (startDateInput?.value && endDateInput?.value) {
          const start = new Date(startDateInput.value);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDateInput.value);
          end.setHours(23, 59, 59, 999);

          filteredSales = filteredSales.filter((s) => {
            const saleDate = new Date(s.date);
            return saleDate >= start && saleDate <= end;
          });
        } else {
          const today = new Date();
          today.setHours(0, 0, 0, 0);
          const tomorrow = new Date(today);
          tomorrow.setDate(tomorrow.getDate() + 1);

          filteredSales = filteredSales.filter((s) => {
            const saleDate = new Date(s.date);
            return saleDate >= today && saleDate < tomorrow;
          });
        }

        // فلترة حسب طريقة الدفع
        if (paymentMethod !== "all") {
          filteredSales = filteredSales.filter(
            (s) => s.paymentMethod === paymentMethod,
          );
        }

        if (user !== "all")
          filteredSales = filteredSales.filter((s) => s.cashier === user);

        if (categoryId !== "all") {
          filteredSales = filteredSales.filter((s) =>
            s.items.some((item) => {
              const product = products.find((p) => p.id === item.id);
              return product && product.category === categoryId;
            }),
          );
        }

        filteredSales.sort((a, b) => new Date(b.date) - new Date(a.date));

        const tbody = document.getElementById("salesTableBody");
        if (filteredSales.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="10" style="text-align:center;">لا توجد مبيعات</td></tr>';
          return;
        }

        tbody.innerHTML = filteredSales
          .map(
            (sale) => `
            <tr>
                <td>${String(sale.invoiceNumber).padStart(4, "0")}</td>
                <td>${new Date(sale.date).toLocaleDateString("en-GB")}</td>
                <td>${new Date(sale.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                <td>${sale.items.map((i) => `${i.name} (${i.quantity})`).join(", ")}</td>
                <td>${getOrderTypeName(sale.orderType)}</td>
                <td>${sale.items.length}</td>
                <td>${(sale.finalTotal || sale.total).toFixed(2)} جنيه</td>
                <td>${getPaymentMethodName(sale.paymentMethod)}</td>
                <td>${sale.cashier}</td>
                <td>
                    <button onclick="viewSaleDetails('${sale.id}')">عرض</button>
                    <button onclick="deleteSale('${sale.id}')">حذف</button>
                </td>
            </tr>
        `,
          )
          .join("");
      }

      function viewSaleDetails(saleId) {
        const sale = sales.find((s) => s.id === saleId);
        if (!sale) return;

        const printWindow = window.open("", "", "width=400,height=600");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head>
                <style>
                    body { font-family: Arial; padding: 20px; }
                    h2 { text-align: center; }
                    .sale-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                    .line { border-top: 1px dashed #000; margin: 10px 0; }
                    table { width: 100%; border-collapse: collapse; }
                    td, th { border: 1px solid #ddd; padding: 5px; text-align: right; }
                </style>
            </head>
            <body>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="sale-logo">
                    <h2>🍖 كفتة على الفحم</h2>
                </div>
                <p>تفاصيل الفاتورة</p>
                <div class="line"></div>
                <p>رقم الفاتورة: ${String(sale.invoiceNumber).padStart(4, "0")}</p>
                <p>التاريخ: ${new Date(sale.date).toLocaleDateString("en-GB")}</p>
                <p>الوقت: ${new Date(sale.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</p>
                <p>نوع الطلب: ${getOrderTypeName(sale.orderType)}</p>
                ${sale.tableNumber ? `<p>طاولة: ${sale.tableNumber}</p>` : ""}
                <p>طريقة الدفع: ${getPaymentMethodName(sale.paymentMethod)}</p>
                <p>الكاشير: ${sale.cashier}</p>
                ${sale.customerName ? `<p>العميل: ${sale.customerName}</p>` : ""}
                ${sale.deliveryNumber ? `<p>رقم التوصيل: ${sale.deliveryNumber}</p>` : ""}
                ${sale.deliveryLocation ? `<p>مكان التوصيل: ${sale.deliveryLocation}</p>` : ""}
                <div class="line"></div>
                <table>
                    <tr><th>المنتج</th><th>الكمية</th><th>السعر</th><th>المجموع</th></tr>
                    ${sale.items
                      .map(
                        (item) => `
                        <tr>
                            <td>${item.name}</td>
                            <td>${item.quantity}</td>
                            <td>${(item.price || 0).toFixed(2)}</td>
                            <td>${((item.price || 0) * item.quantity).toFixed(2)}</td>
                        </tr>
                    `,
                      )
                      .join("")}
                </table>
                <div class="line"></div>
                <p>الإجمالي: ${(sale.finalTotal || sale.total).toFixed(2)} جنيه</p>
                ${sale.orderNotes ? `<p><strong>ملاحظات:</strong> ${sale.orderNotes}</p>` : ""}
            </body>
            </html>
        `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      async function deleteSale(saleId) {
        if (confirm("هل أنت متأكد من حذف هذه الفاتورة؟")) {
          sales = sales.filter((s) => s.id !== saleId);
          const result = await DataManager.saveSales(sales);
          if (result.success) {
            showNotification("✅ تم حذف الفاتورة بنجاح", "success");
          } else {
            showNotification(`⚠️ ${result.message}`, "warning");
          }
          loadAdminSales();
        }
      }

      // ==================== دوال مبيعات المنتجات ====================
      async function loadProductSales() {
        const startDateInput = document.getElementById("productSalesStartDate");
        const endDateInput = document.getElementById("productSalesEndDate");
        const productId = document.getElementById(
          "productSalesFilterProduct",
        ).value;

        let filteredSales = [...sales];

        if (startDateInput?.value && endDateInput?.value) {
          const start = new Date(startDateInput.value);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDateInput.value);
          end.setHours(23, 59, 59, 999);

          filteredSales = filteredSales.filter((s) => {
            const saleDate = new Date(s.date);
            return saleDate >= start && saleDate <= end;
          });
        } else {
          const today = new Date();
          today.setHours(0, 0, 0, 0);
          const tomorrow = new Date(today);
          tomorrow.setDate(tomorrow.getDate() + 1);

          filteredSales = filteredSales.filter((s) => {
            const saleDate = new Date(s.date);
            return saleDate >= today && saleDate < tomorrow;
          });
        }

        if (productId !== "all") {
          filteredSales = filteredSales.filter((s) =>
            s.items.some((item) => item.id === productId),
          );
        }

        const productStats = {};
        const ingredientStats = {};

        filteredSales.forEach((sale) => {
          sale.items.forEach((item) => {
            if (!productStats[item.id]) {
              const product = products.find((p) => p.id === item.id);
              if (product) {
                productStats[item.id] = {
                  name: product.name,
                  salesCount: 0,
                  totalQuantity: 0,
                  totalRevenue: 0,
                  manualIngredients: product.manualIngredients || [],
                };
              }
            }

            if (productStats[item.id]) {
              productStats[item.id].salesCount++;
              productStats[item.id].totalQuantity += item.quantity;
              productStats[item.id].totalRevenue +=
                (item.price || 0) * item.quantity;

              if (productStats[item.id].manualIngredients) {
                productStats[item.id].manualIngredients.forEach(
                  (ingredient) => {
                    const key = `${ingredient.name}_${ingredient.unit || ""}`;
                    if (!ingredientStats[key]) {
                      ingredientStats[key] = {
                        name: ingredient.name,
                        unit: ingredient.unit || "",
                        totalQuantity: 0,
                      };
                    }
                    const ingQty = parseFloat(ingredient.quantity) || 0;
                    ingredientStats[key].totalQuantity +=
                      ingQty * item.quantity;
                  },
                );
              }
            }
          });
        });

        const tbody = document.getElementById("productSalesTableBody");

        if (Object.keys(productStats).length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="5" style="text-align:center;">لا توجد بيانات</td></tr>';
          return;
        }

        tbody.innerHTML = Object.values(productStats)
          .map((product) => {
            const consumedIngredients = [];

            if (product.manualIngredients) {
              product.manualIngredients.forEach((ingredient) => {
                const key = `${ingredient.name}_${ingredient.unit || ""}`;
                if (ingredientStats[key]) {
                  consumedIngredients.push({
                    name: ingredient.name,
                    quantity: ingredientStats[key].totalQuantity,
                    unit: ingredient.unit || "",
                  });
                }
              });
            }

            const ingredientsList = consumedIngredients.length
              ? consumedIngredients
                  .map((i) => `${i.name}: ${i.quantity.toFixed(2)} ${i.unit}`)
                  .join("<br>")
              : "لا يوجد مكونات";

            return `
                <tr>
                    <td>${product.name}</td>
                    <td>${product.salesCount}</td>
                    <td>${product.totalQuantity}</td>
                    <td>${product.totalRevenue.toFixed(2)} جنيه</td>
                    <td style="white-space:normal;">${ingredientsList}</td>
                </tr>
            `;
          })
          .join("");
      }

      // ==================== دوال المصاريف للمدير ====================
      function loadExpenses() {
        const tbody = document.getElementById("expensesTableBody");
        const startDate = document.getElementById(
          "expensesFilterStartDate",
        ).value;
        const endDate = document.getElementById("expensesFilterEndDate").value;
        const user = document.getElementById("expensesFilterUser").value;

        let filteredExpenses = [...expenses];

        if (startDate && endDate) {
          const start = new Date(startDate);
          start.setHours(0, 0, 0, 0);
          const end = new Date(endDate);
          end.setHours(23, 59, 59, 999);

          filteredExpenses = filteredExpenses.filter((e) => {
            const expenseDate = new Date(e.date);
            return expenseDate >= start && expenseDate <= end;
          });
        }

        if (user !== "all")
          filteredExpenses = filteredExpenses.filter((e) => e.user === user);

        filteredExpenses = filteredExpenses.sort(
          (a, b) => new Date(b.date) - new Date(a.date),
        );

        if (filteredExpenses.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="6" style="text-align: center;">لا توجد مصاريف</td></tr>';
          return;
        }

        tbody.innerHTML = filteredExpenses
          .map(
            (expense) => `
            <tr>
                <td>${new Date(expense.date).toLocaleDateString("en-GB")}</td>
                <td>${new Date(expense.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</td>
                <td>${expense.description}</td>
                <td>${expense.amount.toFixed(2)} جنيه</td>
                <td>${expense.user}</td>
                <td>
                    <button class="delete-btn" onclick="deleteExpense('${expense.id}')">
                        <i class="fas fa-trash"></i> حذف
                    </button>
                </td>
            </tr>
        `,
          )
          .join("");
      }

      async function addExpense() {
        const amount = parseFloat(
          document.getElementById("expenseAmount").value,
        );
        const description = document
          .getElementById("expenseDescription")
          .value.trim();
        const date =
          document.getElementById("expenseDate").value ||
          new Date().toISOString().split("T")[0];

        if (!amount || amount <= 0) {
          showNotification("❌ يرجى إدخال مبلغ صحيح", "error");
          return;
        }

        const expense = {
          id: Date.now().toString(),
          amount: amount,
          description: description || "مصروف غير محدد",
          date: new Date(date).toISOString(),
          user: currentUser.name,
        };

        try {
          expenses.push(expense);
          const result = await DataManager.saveExpenses(expenses);
          if (result.success) {
            showNotification("✅ تم إضافة المصروف بنجاح", "success");
          } else {
            showNotification(`⚠️ ${result.message}`, "warning");
          }

          document.getElementById("expenseAmount").value = "";
          document.getElementById("expenseDescription").value = "";
          document.getElementById("expenseDate").value = "";

          loadExpenses();
        } catch (error) {
          console.error("❌ خطأ في إضافة المصروف:", error);
          showNotification("❌ حدث خطأ في إضافة المصروف", "error");
        }
      }

      async function deleteExpense(id) {
        if (confirm("هل أنت متأكد من حذف هذا المصروف؟")) {
          expenses = expenses.filter((e) => e.id !== id);
          const result = await DataManager.saveExpenses(expenses);
          if (result.success) {
            showNotification("✅ تم حذف المصروف بنجاح", "success");
          } else {
            showNotification(`⚠️ ${result.message}`, "warning");
          }
          loadExpenses();
          updateTodayStats();
        }
      }

      // ==================== دوال الأقسام ====================
      async function loadCategories() {
        const container = document.getElementById("categoriesList");
        if (categories.length === 0) {
          container.innerHTML = "<p>لا توجد أقسام حالياً</p>";
          return;
        }

        container.innerHTML = categories
          .map(
            (category) => `
            <div class="category-tag">
                ${category.name}
                <button onclick="deleteCategory('${category.id}')"><i class="fas fa-times"></i></button>
            </div>
        `,
          )
          .join("");
      }

      async function addCategory() {
        const name = document.getElementById("newCategoryName").value.trim();

        if (!name) {
          showNotification("❌ يرجى إدخال اسم القسم", "error");
          return;
        }

        if (categories.find((c) => c.name === name)) {
          showNotification("❌ هذا القسم موجود بالفعل", "error");
          return;
        }

        const newCategory = { id: Date.now().toString(), name: name };

        try {
          categories.push(newCategory);
          const result = await DataManager.saveCategories(categories);
          if (result.success) {
            showNotification("✅ تم إضافة القسم بنجاح", "success");
            document.getElementById("newCategoryName").value = "";
            loadCategories();
            loadAdminProducts();
            updateCategoryButtons();
            updateProductCategorySelect();
            updateCategoryFilterOptions("admin");
            updateCategoryFilterOptions("cashier");
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في إضافة القسم:", error);
          showNotification("❌ حدث خطأ في إضافة القسم", "error");
        }
      }

      async function deleteCategory(categoryId) {
        const category = categories.find((c) => c.id === categoryId);
        if (!category) {
          showNotification("❌ لم يتم العثور على القسم", "error");
          return;
        }

        const productsInCategory = products.filter(
          (p) => p.category === categoryId,
        );
        if (productsInCategory.length > 0) {
          showNotification(
            `❌ لا يمكن حذف القسم "${category.name}" لأنه يحتوي على ${productsInCategory.length} منتجات`,
            "error",
          );
          return;
        }

        if (!confirm(`هل أنت متأكد من حذف قسم "${category.name}"؟`)) return;

        try {
          categories = categories.filter((c) => c.id !== categoryId);
          const result = await DataManager.saveCategories(categories);
          if (result.success) {
            showNotification(
              `✅ تم حذف القسم "${category.name}" بنجاح`,
              "success",
            );
            loadCategories();
            loadAdminProducts();
            updateCategoryButtons();
            updateProductCategorySelect();
            updateCategoryFilterOptions("admin");
            updateCategoryFilterOptions("cashier");
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في حذف القسم:", error);
          showNotification("❌ حدث خطأ أثناء حذف القسم", "error");
        }
      }

      function updateProductCategorySelect() {
        const categorySelect = document.getElementById("productCategory");
        if (categorySelect) {
          categorySelect.innerHTML = categories
            .map(
              (category) =>
                `<option value="${category.id}">${category.name}</option>`,
            )
            .join("");
        }
      }

      function updateCategoryFilterOptions(screen) {
        let filterSelect;
        if (screen === "admin")
          filterSelect = document.getElementById("salesFilterCategory");
        else if (screen === "cashier")
          filterSelect = document.getElementById("cashierFilterCategory");

        if (filterSelect) {
          filterSelect.innerHTML =
            '<option value="all">جميع الأقسام</option>' +
            categories
              .map(
                (category) =>
                  `<option value="${category.id}">${category.name}</option>`,
              )
              .join("");
        }
      }

      // ==================== دوال الموظفين ====================
      async function loadEmployees() {
        await loadFilteredEmployees();
      }

      async function loadFilteredEmployees() {
        const month = document.getElementById("employeeFilterMonth").value;
        const year = document.getElementById("employeeFilterYear").value;
        const status = document.getElementById("employeeFilterStatus").value;

        let filteredEmployees = [...employees];

        if (status !== "all")
          filteredEmployees = filteredEmployees.filter(
            (e) => e.status === status,
          );

        if (month !== "all" && year !== "all") {
          const targetMonth = parseInt(month);
          const targetYear = parseInt(year);

          filteredEmployees = filteredEmployees.filter((employee) => {
            const monthlyLoans =
              employee.loans?.filter((loan) => {
                const loanDate = new Date(loan.date);
                return (
                  loanDate.getMonth() + 1 === targetMonth &&
                  loanDate.getFullYear() === targetYear
                );
              }) || [];

            const monthlyDeductions =
              employee.deductions?.filter((deduction) => {
                const deductionDate = new Date(deduction.date);
                return (
                  deductionDate.getMonth() + 1 === targetMonth &&
                  deductionDate.getFullYear() === targetYear
                );
              }) || [];

            const monthlyVacations =
              employee.vacations?.filter((vacation) => {
                const vacationDate = new Date(vacation.startDate);
                return (
                  vacationDate.getMonth() + 1 === targetMonth &&
                  vacationDate.getFullYear() === targetYear
                );
              }) || [];

            return (
              monthlyLoans.length > 0 ||
              monthlyDeductions.length > 0 ||
              monthlyVacations.length > 0
            );
          });
        }

        displayEmployeesList(filteredEmployees);
      }

      function displayEmployeesList(filteredEmployees) {
        const container = document.getElementById("employeesList");

        if (filteredEmployees.length === 0) {
          container.innerHTML =
            '<div class="empty-state"><div class="empty-state-icon"><i class="fas fa-users"></i></div><p>لا يوجد موظفين حالياً</p></div>';
          return;
        }

        container.innerHTML = filteredEmployees
          .map((employee) => {
            const currentMonth = new Date().getMonth() + 1;
            const currentYear = new Date().getFullYear();

            const monthlyLoans =
              employee.loans?.filter((loan) => {
                const loanDate = new Date(loan.date);
                return (
                  loanDate.getMonth() + 1 === currentMonth &&
                  loanDate.getFullYear() === currentYear
                );
              }) || [];

            const monthlyDeductions =
              employee.deductions?.filter((deduction) => {
                const deductionDate = new Date(deduction.date);
                return (
                  deductionDate.getMonth() + 1 === currentMonth &&
                  deductionDate.getFullYear() === currentYear
                );
              }) || [];

            const monthlyVacations =
              employee.vacations?.filter((vacation) => {
                const vacationDate = new Date(vacation.startDate);
                return (
                  vacationDate.getMonth() + 1 === currentMonth &&
                  vacationDate.getFullYear() === currentYear
                );
              }) || [];

            const totalLoans = monthlyLoans.reduce(
              (sum, loan) => sum + loan.amount,
              0,
            );
            const totalDeductions = monthlyDeductions.reduce(
              (sum, deduction) => sum + deduction.amount,
              0,
            );
            const totalVacationsDays = monthlyVacations.reduce(
              (sum, vacation) => {
                const start = new Date(vacation.startDate);
                const end = new Date(vacation.endDate);
                const days =
                  Math.ceil((end - start) / (1000 * 60 * 60 * 24)) + 1;
                return sum + days;
              },
              0,
            );

            const netSalary = employee.salary - totalDeductions;

            return `
                <div class="employee-card">
                    <div class="employee-card-header">
                        <div class="employee-avatar">${employee.name.charAt(0).toUpperCase()}</div>
                        <div class="employee-info">
                            <h3>${employee.name}</h3>
                            <p>${employee.position} - ${employee.status === "active" ? "نشط" : "غير نشط"}</p>
                        </div>
                    </div>
                    <div class="employee-details">
                        <div class="employee-detail"><span class="employee-detail-label">رقم الهاتف:</span><span class="employee-detail-value">${employee.phone}</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">الراتب الأساسي:</span><span class="employee-detail-value">${employee.salary.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">تاريخ التعيين:</span><span class="employee-detail-value">${employee.hireDate}</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">السلفيات الشهرية:</span><span class="employee-detail-value">${totalLoans.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">الخصومات الشهرية:</span><span class="employee-detail-value">${totalDeductions.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">إجازات الشهر:</span><span class="employee-detail-value">${totalVacationsDays} يوم</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">صافي الراتب:</span><span class="employee-detail-value">${netSalary.toFixed(2)} جنيه</span></div>
                    </div>
                    <div class="employee-actions">
                        <button class="btn-loan" onclick="manageEmployee('${employee.id}', 'loan')"><i class="fas fa-hand-holding-usd"></i> سلفية</button>
                        <button class="btn-vacation" onclick="manageEmployee('${employee.id}', 'vacation')"><i class="fas fa-umbrella-beach"></i> إجازة</button>
                        <button class="btn-deduction" onclick="manageEmployee('${employee.id}', 'deduction')"><i class="fas fa-minus-circle"></i> خصم</button>
                        <button class="btn-salary" onclick="manageEmployee('${employee.id}', 'salary')"><i class="fas fa-money-check-alt"></i> راتب</button>
                        <button class="btn-info" onclick="viewEmployeeDetails('${employee.id}')"><i class="fas fa-eye"></i> تفاصيل</button>
                        <button class="btn-print" onclick="printEmployeeMonthlyReport('${employee.id}')"><i class="fas fa-print"></i> طباعة تقرير</button>
                        <button class="btn-edit" onclick="openEditEmployeeModal('${employee.id}')"><i class="fas fa-edit"></i> تعديل</button>
                        <button class="btn-delete" onclick="deleteEmployee('${employee.id}')"><i class="fas fa-trash"></i> حذف</button>
                    </div>
                </div>
            `;
          })
          .join("");
      }

      function viewEmployeeDetails(employeeId) {
        const employee = employees.find((e) => e.id === employeeId);
        if (!employee) return;

        const currentMonth = new Date().getMonth() + 1;
        const currentYear = new Date().getFullYear();

        const monthlyLoans =
          employee.loans?.filter((loan) => {
            const loanDate = new Date(loan.date);
            return (
              loanDate.getMonth() + 1 === currentMonth &&
              loanDate.getFullYear() === currentYear
            );
          }) || [];

        const monthlyDeductions =
          employee.deductions?.filter((deduction) => {
            const deductionDate = new Date(deduction.date);
            return (
              deductionDate.getMonth() + 1 === currentMonth &&
              deductionDate.getFullYear() === currentYear
            );
          }) || [];

        const monthlyVacations =
          employee.vacations?.filter((vacation) => {
            const vacationDate = new Date(vacation.startDate);
            return (
              vacationDate.getMonth() + 1 === currentMonth &&
              vacationDate.getFullYear() === currentYear
            );
          }) || [];

        const totalLoans = monthlyLoans.reduce(
          (sum, loan) => sum + loan.amount,
          0,
        );
        const totalDeductions = monthlyDeductions.reduce(
          (sum, deduction) => sum + deduction.amount,
          0,
        );

        const modalContent = `
            <div class="employee-details-modal">
                <h3>${employee.name}</h3>
                <p><strong>الوظيفة:</strong> ${employee.position}</p>
                <p><strong>الحالة:</strong> ${employee.status === "active" ? "نشط" : "غير نشط"}</p>
                <p><strong>رقم الهاتف:</strong> ${employee.phone}</p>
                <p><strong>تاريخ التعيين:</strong> ${employee.hireDate}</p>
                
                <div class="monthly-summary">
                    <h4>ملخص الشهر الحالي (${currentMonth}/${currentYear})</h4>
                    <p><strong>الراتب الأساسي:</strong> ${employee.salary.toFixed(2)} جنيه</p>
                    <p><strong>إجمالي السلفيات:</strong> ${totalLoans.toFixed(2)} جنيه</p>
                    <p><strong>إجمالي الخصومات:</strong> ${totalDeductions.toFixed(2)} جنيه</p>
                    <p><strong>صافي الراتب:</strong> ${(employee.salary - totalDeductions).toFixed(2)} جنيه</p>
                </div>
                
                ${
                  monthlyLoans.length > 0
                    ? `
                    <div class="details-section">
                        <h5>السلفيات:</h5>
                        <ul>${monthlyLoans.map((loan) => `<li>${loan.date}: ${loan.amount.toFixed(2)} جنيه - ${loan.reason || "غير محدد"}</li>`).join("")}</ul>
                    </div>
                `
                    : ""
                }
                
                ${
                  monthlyDeductions.length > 0
                    ? `
                    <div class="details-section">
                        <h5>الخصومات:</h5>
                        <ul>${monthlyDeductions.map((deduction) => `<li>${deduction.date}: ${deduction.amount.toFixed(2)} جنيه - ${deduction.reason || "غير محدد"}</li>`).join("")}</ul>
                    </div>
                `
                    : ""
                }
                
                ${
                  monthlyVacations.length > 0
                    ? `
                    <div class="details-section">
                        <h5>الإجازات:</h5>
                        <ul>${monthlyVacations.map((vacation) => `<li>${vacation.startDate} إلى ${vacation.endDate}: ${vacation.type === "annual" ? "سنوية" : vacation.type === "sick" ? "مرضية" : vacation.type === "emergency" ? "طارئة" : "بدون راتب"}</li>`).join("")}</ul>
                    </div>
                `
                    : ""
                }
            </div>
        `;

        document.getElementById("employeeModalTitle").innerHTML =
          '<i class="fas fa-user"></i> تفاصيل الموظف';
        document.getElementById("employeeModalSubtitle").textContent =
          employee.name;
        document.getElementById("employeeModalContent").innerHTML =
          modalContent;
        document.getElementById("employeeModal").style.display = "flex";
        document.getElementById("saveEmployeeActionBtn").style.display = "none";
      }

      async function resetMonthlyData() {
        if (
          !confirm(
            "⚠️ هل أنت متأكد من تصفير البيانات الشهرية؟\nسيتم حذف جميع السلفيات والخصومات والإجازات لهذا الشهر.",
          )
        )
          return;

        const currentMonth = new Date().getMonth() + 1;
        const currentYear = new Date().getFullYear();

        try {
          employees.forEach((employee) => {
            if (employee.loans) {
              employee.loans = employee.loans.filter((loan) => {
                const loanDate = new Date(loan.date);
                return !(
                  loanDate.getMonth() + 1 === currentMonth &&
                  loanDate.getFullYear() === currentYear
                );
              });
            }

            if (employee.deductions) {
              employee.deductions = employee.deductions.filter((deduction) => {
                const deductionDate = new Date(deduction.date);
                return !(
                  deductionDate.getMonth() + 1 === currentMonth &&
                  deductionDate.getFullYear() === currentYear
                );
              });
            }

            if (employee.vacations) {
              employee.vacations = employee.vacations.filter((vacation) => {
                const vacationDate = new Date(vacation.startDate);
                return !(
                  vacationDate.getMonth() + 1 === currentMonth &&
                  vacationDate.getFullYear() === currentYear
                );
              });
            }
          });

          const result = await DataManager.saveEmployees(employees);
          if (result.success) {
            showNotification("✅ تم تصفير البيانات الشهرية بنجاح", "success");
            loadEmployees();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في تصفير البيانات الشهرية:", error);
          showNotification("❌ حدث خطأ في تصفير البيانات", "error");
        }
      }

      function generateMonthlyReport() {
        const month = document.getElementById("employeeFilterMonth").value;
        const year = document.getElementById("employeeFilterYear").value;

        if (month === "all" || year === "all") {
          showNotification("❌ يرجى تحديد شهر وسنة معينة", "error");
          return;
        }

        const targetMonth = parseInt(month);
        const targetYear = parseInt(year);

        const monthNames = [
          "يناير",
          "فبراير",
          "مارس",
          "أبريل",
          "مايو",
          "يونيو",
          "يوليو",
          "أغسطس",
          "سبتمبر",
          "أكتوبر",
          "نوفمبر",
          "ديسمبر",
        ];

        let reportHTML = `
            <div class="employee-report">
                <div style="text-align: center; margin-bottom: 20px;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" 
                         alt="${restaurantInfo.name}" 
                         style="width: 100px; height: 100px; border-radius: 50%; margin: 0 auto 10px; display: block;">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                    <h3>تقرير الموظفين الشهري</h3>
                    <h4>شهر: ${monthNames[targetMonth - 1]} ${targetYear}</h4>
                    <p>تاريخ التقرير: ${new Date().toLocaleDateString("ar-EG")}</p>
                    <p>وقت التقرير: ${new Date().toLocaleTimeString("ar-EG")}</p>
                </div>
                
                <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                    <thead>
                        <tr style="background: var(--primary-color);">
                            <th style="border: 1px solid #000; padding: 10px;">اسم الموظف</th>
                            <th style="border: 1px solid #000; padding: 10px;">الوظيفة</th>
                            <th style="border: 1px solid #000; padding: 10px;">الراتب الأساسي</th>
                            <th style="border: 1px solid #000; padding: 10px;">السلفيات</th>
                            <th style="border: 1px solid #000; padding: 10px;">الخصومات</th>
                            <th style="border: 1px solid #000; padding: 10px;">صافي الراتب</th>
                            <th style="border: 1px solid #000; padding: 10px;">عدد أيام الإجازة</th>
                        </tr>
                    </thead>
                    <tbody>
        `;

        let totalSalaries = 0,
          totalLoans = 0,
          totalDeductions = 0,
          totalNetSalaries = 0;

        employees.forEach((employee) => {
          if (employee.status === "active") {
            const monthlyLoans =
              employee.loans?.filter((loan) => {
                const loanDate = new Date(loan.date);
                return (
                  loanDate.getMonth() + 1 === targetMonth &&
                  loanDate.getFullYear() === targetYear
                );
              }) || [];

            const monthlyDeductions =
              employee.deductions?.filter((deduction) => {
                const deductionDate = new Date(deduction.date);
                return (
                  deductionDate.getMonth() + 1 === targetMonth &&
                  deductionDate.getFullYear() === targetYear
                );
              }) || [];

            const monthlyVacations =
              employee.vacations?.filter((vacation) => {
                const vacationDate = new Date(vacation.startDate);
                return (
                  vacationDate.getMonth() + 1 === targetMonth &&
                  vacationDate.getFullYear() === targetYear
                );
              }) || [];

            const totalLoansAmount = monthlyLoans.reduce(
              (sum, loan) => sum + loan.amount,
              0,
            );
            const totalDeductionsAmount = monthlyDeductions.reduce(
              (sum, deduction) => sum + deduction.amount,
              0,
            );
            const totalVacationsDays = monthlyVacations.reduce(
              (sum, vacation) => {
                const start = new Date(vacation.startDate);
                const end = new Date(vacation.endDate);
                const days =
                  Math.ceil((end - start) / (1000 * 60 * 60 * 24)) + 1;
                return sum + days;
              },
              0,
            );

            const netSalary = employee.salary - totalDeductionsAmount;

            totalSalaries += employee.salary;
            totalLoans += totalLoansAmount;
            totalDeductions += totalDeductionsAmount;
            totalNetSalaries += netSalary;

            reportHTML += `
                    <tr>
                        <td style="border: 1px solid #000; padding: 8px;">${employee.name}</td>
                        <td style="border: 1px solid #000; padding: 8px;">${employee.position}</td>
                        <td style="border: 1px solid #000; padding: 8px; text-align: center;">${employee.salary.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 8px; text-align: center;">${totalLoansAmount.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 8px; text-align: center;">${totalDeductionsAmount.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 8px; text-align: center; font-weight: bold;">${netSalary.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 8px; text-align: center;">${totalVacationsDays}</td>
                    </tr>
                `;
          }
        });

        reportHTML += `
                    <tr style="background: #f0f8ff; font-weight: bold;">
                        <td colspan="2" style="border: 1px solid #000; padding: 10px; text-align: center;">الإجمالي</td>
                        <td style="border: 1px solid #000; padding: 10px; text-align: center;">${totalSalaries.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 10px; text-align: center;">${totalLoans.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 10px; text-align: center;">${totalDeductions.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 10px; text-align: center;">${totalNetSalaries.toFixed(2)}</td>
                        <td style="border: 1px solid #000; padding: 10px; text-align: center;">-</td>
                    </tr>
                </tbody>
            </table>
            
            <div style="margin-top: 40px;">
                <div style="display: flex; justify-content: space-between; margin-top: 50px;">
                    <div style="text-align: center; width: 45%;">
                        <div style="border-top: 1px solid #000; padding-top: 10px; margin-top: 40px;">
                            <p>توقيع المدير</p>
                            <p style="margin-top: 20px;">${currentUser ? currentUser.name : "المدير"}</p>
                        </div>
                    </div>
                    <div style="text-align: center; width: 45%;">
                        <div style="border-top: 1px solid #000; padding-top: 10px; margin-top: 40px;">
                            <p>توقيع المحاسب</p>
                            <p style="margin-top: 20px;">.....................</p>
                        </div>
                    </div>
                </div>
                
                <div style="text-align: center; margin-top: 30px; font-size: 12px; color: #666;">
                    <p>تم إنشاء هذا التقرير بواسطة نظام كفتة على الفحم</p>
                    <p>General Manager Mohammed Hashem</p>
                </div>
            </div>
        </div>
        `;

        localStorage.setItem("employeeMonthlyReport", reportHTML);
        showPrintReportModal(reportHTML);
      }

      function showPrintReportModal(content) {
        document.getElementById("printReportContent").innerHTML = content;
        document.getElementById("printEmployeeReportModal").style.display =
          "flex";
      }

      function closePrintReportModal() {
        document.getElementById("printEmployeeReportModal").style.display =
          "none";
      }

      function printEmployeeReportNow() {
        const printWindow = window.open("", "_blank");
        printWindow.document.write(`
            <!DOCTYPE html>
            <html dir="rtl">
            <head><title>تقرير الموظفين الشهري</title>
            <style>body { font-family: Arial; padding: 20px; }</style></head>
            <body>${document.getElementById("printReportContent").innerHTML}</body>
            </html>
        `);
        printWindow.document.close();
        printWindow.print();
      }

      function printEmployeeMonthlyReport(employeeId) {
        const employee = employees.find((e) => e.id === employeeId);
        if (!employee) return;

        const currentMonth = new Date().getMonth() + 1;
        const currentYear = new Date().getFullYear();
        const monthNames = [
          "يناير",
          "فبراير",
          "مارس",
          "أبريل",
          "مايو",
          "يونيو",
          "يوليو",
          "أغسطس",
          "سبتمبر",
          "أكتوبر",
          "نوفمبر",
          "ديسمبر",
        ];

        const monthlyLoans =
          employee.loans?.filter((loan) => {
            const loanDate = new Date(loan.date);
            return (
              loanDate.getMonth() + 1 === currentMonth &&
              loanDate.getFullYear() === currentYear
            );
          }) || [];

        const monthlyDeductions =
          employee.deductions?.filter((deduction) => {
            const deductionDate = new Date(deduction.date);
            return (
              deductionDate.getMonth() + 1 === currentMonth &&
              deductionDate.getFullYear() === currentYear
            );
          }) || [];

        const monthlyVacations =
          employee.vacations?.filter((vacation) => {
            const vacationDate = new Date(vacation.startDate);
            return (
              vacationDate.getMonth() + 1 === currentMonth &&
              vacationDate.getFullYear() === currentYear
            );
          }) || [];

        const totalLoans = monthlyLoans.reduce(
          (sum, loan) => sum + loan.amount,
          0,
        );
        const totalDeductions = monthlyDeductions.reduce(
          (sum, deduction) => sum + deduction.amount,
          0,
        );
        const netSalary = employee.salary - totalDeductions;

        const reportHTML = `
            <div class="employee-report" style="font-family: Arial; padding: 20px;">
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" 
                         style="width: 100px; height: 100px; border-radius: 50%;">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                    <h3>تقرير راتب الموظف</h3>
                    <h4>شهر: ${monthNames[currentMonth - 1]} ${currentYear}</h4>
                </div>
                
                <div><h4>معلومات الموظف:</h4>
                <table style="width:100%; border-collapse:collapse;">
                    <tr><td><strong>الاسم:</strong></td><td>${employee.name}</td></tr>
                    <tr><td><strong>الوظيفة:</strong></td><td>${employee.position}</td></tr>
                    <tr><td><strong>رقم الهاتف:</strong></td><td>${employee.phone}</td></tr>
                    <tr><td><strong>تاريخ التعيين:</strong></td><td>${employee.hireDate}</td></tr>
                </table></div>
                
                <div><h4>تفاصيل الراتب:</h4>
                <table style="width:100%; border-collapse:collapse;">
                    <tr><td>الراتب الأساسي:</td><td>${employee.salary.toFixed(2)} جنيه</td></tr>
                    ${monthlyLoans.length > 0 ? `<tr><td>السلفيات (${monthlyLoans.length}):</td><td>${totalLoans.toFixed(2)} جنيه</td></tr>` : ""}
                    ${monthlyDeductions.length > 0 ? `<tr><td>الخصومات (${monthlyDeductions.length}):</td><td>${totalDeductions.toFixed(2)} جنيه</td></tr>` : ""}
                    <tr style="background:#f0f8ff;"><td><strong>صافي الراتب المستحق:</strong></td><td><strong>${netSalary.toFixed(2)} جنيه</strong></td></tr>
                </table></div>
                
                <div style="display:flex; justify-content:space-between; margin-top:50px;">
                    <div style="text-align:center; width:45%; border-top:1px solid #000; padding-top:10px;">
                        <p>توقيع المدير</p><p>${currentUser ? currentUser.name : "المدير"}</p>
                    </div>
                    <div style="text-align:center; width:45%; border-top:1px solid #000; padding-top:10px;">
                        <p>توقيع الموظف</p><p>${employee.name}</p>
                    </div>
                </div>
            </div>
        `;

        const printWindow = window.open("", "_blank");
        printWindow.document.write(`
            <!DOCTYPE html>
            <html dir="rtl"><head><title>تقرير راتب - ${employee.name}</title>
            <style>body { font-family: Arial; padding: 20px; }</style></head>
            <body>${reportHTML}</body></html>
        `);
        printWindow.document.close();
        printWindow.print();
      }

      function printEmployeesReport() {
        generateMonthlyReport();
      }

      function exportEmployeesToExcel() {
        try {
          const currentMonth = new Date().getMonth() + 1;
          const currentYear = new Date().getFullYear();

          const data = [];
          data.push(["تقرير الموظفين", "", "", "", "", ""]);
          data.push(["شهر:", `${currentMonth}/${currentYear}`, "", "", "", ""]);
          data.push([
            "تاريخ التصدير:",
            new Date().toLocaleDateString("ar-EG"),
            "",
            "",
            "",
            "",
          ]);
          data.push([]);

          data.push([
            "اسم الموظف",
            "الوظيفة",
            "الراتب الأساسي",
            "السلفيات",
            "الخصومات",
            "صافي الراتب",
            "عدد أيام الإجازة",
            "الحالة",
          ]);

          employees.forEach((employee) => {
            const monthlyLoans =
              employee.loans?.filter((loan) => {
                const loanDate = new Date(loan.date);
                return (
                  loanDate.getMonth() + 1 === currentMonth &&
                  loanDate.getFullYear() === currentYear
                );
              }) || [];

            const monthlyDeductions =
              employee.deductions?.filter((deduction) => {
                const deductionDate = new Date(deduction.date);
                return (
                  deductionDate.getMonth() + 1 === currentMonth &&
                  deductionDate.getFullYear() === currentYear
                );
              }) || [];

            const monthlyVacations =
              employee.vacations?.filter((vacation) => {
                const vacationDate = new Date(vacation.startDate);
                return (
                  vacationDate.getMonth() + 1 === currentMonth &&
                  vacationDate.getFullYear() === currentYear
                );
              }) || [];

            const totalLoans = monthlyLoans.reduce(
              (sum, loan) => sum + loan.amount,
              0,
            );
            const totalDeductions = monthlyDeductions.reduce(
              (sum, deduction) => sum + deduction.amount,
              0,
            );
            const totalVacationsDays = monthlyVacations.reduce(
              (sum, vacation) => {
                const start = new Date(vacation.startDate);
                const end = new Date(vacation.endDate);
                const days =
                  Math.ceil((end - start) / (1000 * 60 * 60 * 24)) + 1;
                return sum + days;
              },
              0,
            );

            const netSalary = employee.salary - totalDeductions;

            data.push([
              employee.name,
              employee.position,
              employee.salary,
              totalLoans,
              totalDeductions,
              netSalary,
              totalVacationsDays,
              employee.status === "active" ? "نشط" : "غير نشط",
            ]);
          });

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "الموظفين");

          const wscols = [
            { wch: 25 },
            { wch: 20 },
            { wch: 15 },
            { wch: 15 },
            { wch: 15 },
            { wch: 15 },
            { wch: 15 },
            { wch: 10 },
          ];
          ws["!cols"] = wscols;

          const today = new Date().toISOString().split("T")[0];
          XLSX.writeFile(wb, `تقرير_الموظفين_${today}.xlsx`);

          showNotification(
            "✅ تم تصدير بيانات الموظفين إلى Excel بنجاح",
            "success",
          );
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification("❌ حدث خطأ أثناء التصدير إلى Excel", "error");
        }
      }

      function initializeYearFilter() {
        const yearSelect = document.getElementById("employeeFilterYear");
        if (!yearSelect) return;

        const currentYear = new Date().getFullYear();
        yearSelect.innerHTML = '<option value="all">جميع السنوات</option>';

        for (let year = 2020; year <= currentYear + 1; year++) {
          const option = document.createElement("option");
          option.value = year;
          option.textContent = year;
          if (year === currentYear) option.selected = true;
          yearSelect.appendChild(option);
        }
      }

      async function addEmployee() {
        const name = document.getElementById("employeeFullName").value.trim();
        const phone = document.getElementById("employeePhone").value.trim();
        const salary = parseFloat(
          document.getElementById("employeeSalary").value,
        );
        const position = document
          .getElementById("employeePosition")
          .value.trim();
        const hireDate = document.getElementById("employeeHireDate").value;

        if (!name || !phone || !salary || !position || !hireDate) {
          showNotification("❌ يرجى ملء جميع الحقول", "error");
          return;
        }

        const newEmployee = {
          id: Date.now().toString(),
          name: name,
          phone: phone,
          salary: salary,
          position: position,
          hireDate: hireDate,
          loans: [],
          vacations: [],
          deductions: [],
          status: "active",
          createdAt: new Date().toISOString(),
        };

        try {
          employees.push(newEmployee);
          const result = await DataManager.saveEmployees(employees);

          if (result.success) {
            showNotification("✅ تم إضافة الموظف بنجاح", "success");
            document.getElementById("employeeFullName").value = "";
            document.getElementById("employeePhone").value = "";
            document.getElementById("employeeSalary").value = "";
            document.getElementById("employeePosition").value = "";
            document.getElementById("employeeHireDate").value = "";
            loadEmployees();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في إضافة الموظف:", error);
          showNotification("❌ حدث خطأ في إضافة الموظف", "error");
        }
      }

      function manageEmployee(employeeId, action) {
        currentEmployeeId = employeeId;
        currentEmployeeAction = action;
        const employee = employees.find((e) => e.id === employeeId);

        if (!employee) return;

        let modalTitle = "",
          modalSubtitle = "",
          modalContent = "";

        switch (action) {
          case "loan":
            modalTitle = "إضافة سلفية";
            modalSubtitle = `للموظف: ${employee.name}`;
            modalContent = `
                    <div class="form-group">
                        <label>مبلغ السلفية (جنيه)</label>
                        <input type="number" id="loanAmount" placeholder="0.00">
                    </div>
                    <div class="form-group">
                        <label>تاريخ السلفية</label>
                        <input type="date" id="loanDate" value="${new Date().toISOString().split("T")[0]}">
                    </div>
                    <div class="form-group">
                        <label>سبب السلفية</label>
                        <input type="text" id="loanReason" placeholder="سبب السلفية">
                    </div>
                `;
            break;

          case "vacation":
            modalTitle = "تسجيل إجازة";
            modalSubtitle = `للموظف: ${employee.name}`;
            modalContent = `
                    <div class="form-group">
                        <label>تاريخ بداية الإجازة</label>
                        <input type="date" id="vacationStartDate" value="${new Date().toISOString().split("T")[0]}">
                    </div>
                    <div class="form-group">
                        <label>تاريخ نهاية الإجازة</label>
                        <input type="date" id="vacationEndDate" value="${new Date().toISOString().split("T")[0]}">
                    </div>
                    <div class="form-group">
                        <label>نوع الإجازة</label>
                        <select id="vacationType">
                            <option value="annual">سنوية</option>
                            <option value="sick">مرضية</option>
                            <option value="emergency">طارئة</option>
                            <option value="unpaid">بدون راتب</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>ملاحظات</label>
                        <input type="text" id="vacationNotes" placeholder="ملاحظات عن الإجازة">
                    </div>
                `;
            break;

          case "deduction":
            modalTitle = "تسجيل خصم";
            modalSubtitle = `للموظف: ${employee.name}`;
            modalContent = `
                    <div class="form-group">
                        <label>مبلغ الخصم (جنيه)</label>
                        <input type="number" id="deductionAmount" placeholder="0.00">
                    </div>
                    <div class="form-group">
                        <label>تاريخ الخصم</label>
                        <input type="date" id="deductionDate" value="${new Date().toISOString().split("T")[0]}">
                    </div>
                    <div class="form-group">
                        <label>سبب الخصم</label>
                        <input type="text" id="deductionReason" placeholder="سبب الخصم">
                    </div>
                `;
            break;

          case "salary":
            modalTitle = "صرف راتب";
            modalSubtitle = `للموظف: ${employee.name}`;
            const totalLoans =
              employee.loans?.reduce((sum, loan) => sum + loan.amount, 0) || 0;
            const totalDeductions =
              employee.deductions?.reduce(
                (sum, deduction) => sum + deduction.amount,
                0,
              ) || 0;
            const netSalary = employee.salary - totalDeductions;

            modalContent = `
                    <div class="employee-details">
                        <div class="employee-detail"><span class="employee-detail-label">الراتب الأساسي:</span><span class="employee-detail-value">${employee.salary.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">إجمالي السلف:</span><span class="employee-detail-value">${totalLoans.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">إجمالي الخصومات:</span><span class="employee-detail-value">${totalDeductions.toFixed(2)} جنيه</span></div>
                        <div class="employee-detail"><span class="employee-detail-label">صافي الراتب:</span><span class="employee-detail-value">${netSalary.toFixed(2)} جنيه</span></div>
                    </div>
                    <div class="form-group">
                        <label>تاريخ صرف الراتب</label>
                        <input type="date" id="salaryDate" value="${new Date().toISOString().split("T")[0]}">
                    </div>
                    <div class="form-group">
                        <label>ملاحظات</label>
                        <input type="text" id="salaryNotes" placeholder="ملاحظات عن صرف الراتب">
                    </div>
                `;
            break;
        }

        document.getElementById("employeeModalTitle").innerHTML =
          `<i class="fas fa-user"></i> ${modalTitle}`;
        document.getElementById("employeeModalSubtitle").textContent =
          modalSubtitle;
        document.getElementById("employeeModalContent").innerHTML =
          modalContent;
        document.getElementById("employeeModal").style.display = "flex";

        document.getElementById("saveEmployeeActionBtn").onclick =
          saveEmployeeAction;
      }

      function closeEmployeeModal() {
        document.getElementById("employeeModal").style.display = "none";
        currentEmployeeId = "";
        currentEmployeeAction = "";
      }

      async function saveEmployeeAction() {
        const employee = employees.find((e) => e.id === currentEmployeeId);
        if (!employee) return;

        switch (currentEmployeeAction) {
          case "loan":
            const loanAmount = parseFloat(
              document.getElementById("loanAmount").value,
            );
            const loanDate = document.getElementById("loanDate").value;
            const loanReason = document
              .getElementById("loanReason")
              .value.trim();

            if (!loanAmount || loanAmount <= 0) {
              showNotification("❌ يرجى إدخال مبلغ صحيح", "error");
              return;
            }

            if (!employee.loans) employee.loans = [];
            employee.loans.push({
              id: Date.now().toString(),
              amount: loanAmount,
              date: loanDate,
              reason: loanReason || "سلفية",
              status: "pending",
            });
            break;

          case "vacation":
            const vacationStartDate =
              document.getElementById("vacationStartDate").value;
            const vacationEndDate =
              document.getElementById("vacationEndDate").value;
            const vacationType = document.getElementById("vacationType").value;
            const vacationNotes = document
              .getElementById("vacationNotes")
              .value.trim();

            if (!vacationStartDate || !vacationEndDate) {
              showNotification(
                "❌ يرجى تحديد تاريخي بداية ونهاية الإجازة",
                "error",
              );
              return;
            }

            if (!employee.vacations) employee.vacations = [];
            employee.vacations.push({
              id: Date.now().toString(),
              startDate: vacationStartDate,
              endDate: vacationEndDate,
              type: vacationType,
              notes: vacationNotes || "إجازة",
              status: "approved",
            });
            break;

          case "deduction":
            const deductionAmount = parseFloat(
              document.getElementById("deductionAmount").value,
            );
            const deductionDate =
              document.getElementById("deductionDate").value;
            const deductionReason = document
              .getElementById("deductionReason")
              .value.trim();

            if (!deductionAmount || deductionAmount <= 0) {
              showNotification("❌ يرجى إدخال مبلغ صحيح", "error");
              return;
            }

            if (!employee.deductions) employee.deductions = [];
            employee.deductions.push({
              id: Date.now().toString(),
              amount: deductionAmount,
              date: deductionDate,
              reason: deductionReason || "خصم",
              status: "applied",
            });
            break;

          case "salary":
            const salaryDate = document.getElementById("salaryDate").value;
            const salaryNotes = document
              .getElementById("salaryNotes")
              .value.trim();

            if (!employee.salaryPayments) employee.salaryPayments = [];
            const totalLoans =
              employee.loans?.reduce((sum, loan) => sum + loan.amount, 0) || 0;
            const totalDeductions =
              employee.deductions?.reduce(
                (sum, deduction) => sum + deduction.amount,
                0,
              ) || 0;
            const netSalary = employee.salary - totalDeductions;

            employee.salaryPayments.push({
              id: Date.now().toString(),
              date: salaryDate,
              basicSalary: employee.salary,
              loans: totalLoans,
              deductions: totalDeductions,
              netSalary: netSalary,
              notes: salaryNotes || "صرف راتب",
              status: "paid",
            });
            break;
        }

        try {
          const result = await DataManager.saveEmployees(employees);
          if (result.success) {
            showNotification("✅ تم حفظ العملية بنجاح", "success");
            loadEmployees();
            closeEmployeeModal();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في حفظ العملية:", error);
          showNotification("❌ حدث خطأ في حفظ العملية", "error");
        }
      }

      function openEditEmployeeModal(employeeId) {
        const employee = employees.find((e) => e.id === employeeId);
        if (!employee) return;

        document.getElementById("editEmployeeFullName").value = employee.name;
        document.getElementById("editEmployeePhone").value = employee.phone;
        document.getElementById("editEmployeeSalary").value = employee.salary;
        document.getElementById("editEmployeePosition").value =
          employee.position;
        document.getElementById("editEmployeeStatus").value = employee.status;

        document.getElementById("editEmployeeModal").style.display = "flex";
        document.getElementById("editEmployeeModal").dataset.employeeId =
          employeeId;
      }

      function closeEditEmployeeModal() {
        document.getElementById("editEmployeeModal").style.display = "none";
      }

      async function saveEditedEmployee() {
        const employeeId =
          document.getElementById("editEmployeeModal").dataset.employeeId;
        const employee = employees.find((e) => e.id === employeeId);
        if (!employee) return;

        employee.name = document
          .getElementById("editEmployeeFullName")
          .value.trim();
        employee.phone = document
          .getElementById("editEmployeePhone")
          .value.trim();
        employee.salary = parseFloat(
          document.getElementById("editEmployeeSalary").value,
        );
        employee.position = document
          .getElementById("editEmployeePosition")
          .value.trim();
        employee.status = document.getElementById("editEmployeeStatus").value;

        try {
          const result = await DataManager.saveEmployees(employees);
          if (result.success) {
            showNotification("✅ تم تحديث بيانات الموظف بنجاح", "success");
            loadEmployees();
            closeEditEmployeeModal();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في تحديث بيانات الموظف:", error);
          showNotification("❌ حدث خطأ في تحديث بيانات الموظف", "error");
        }
      }

      async function deleteEmployee(employeeId) {
        if (confirm("هل أنت متأكد من حذف هذا الموظف؟")) {
          employees = employees.filter((e) => e.id !== employeeId);
          const result = await DataManager.saveEmployees(employees);
          if (result.success) {
            showNotification("✅ تم حذف الموظف بنجاح", "success");
            loadEmployees();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        }
      }

      // ==================== دوال المستخدمين ====================
      async function loadUsers() {
        users = await DataManager.getUsers();
        window.users = users;

        const container = document.getElementById("usersList");
        container.innerHTML = users
          .map(
            (user) => `
            <div class="user-card">
                <div class="user-card-header">
                    <div class="user-avatar">${user.name.charAt(0).toUpperCase()}</div>
                    <div class="user-info">
                        <h3>${user.name}</h3>
                        <p>${user.role === "admin" ? "مدير" : "كاشير"}</p>
                    </div>
                </div>
                <div class="user-role ${user.role}">${user.role === "admin" ? "مدير" : "كاشير"}</div>
                <p>اسم المستخدم: ${user.username}</p>
                <div class="user-actions">
                    <button class="edit-btn" onclick="editUser('${user.username}')"><i class="fas fa-edit"></i> تعديل</button>
                    <button class="delete-btn" onclick="deleteUser('${user.username}')"><i class="fas fa-trash"></i> حذف</button>
                </div>
            </div>
        `,
          )
          .join("");

        updateUserFilterOptions();
        window.dispatchEvent(new CustomEvent("userDataUpdated"));
      }

      function updateUserFilterOptions() {
        const users = window.users || [];

        const salesFilterUser = document.getElementById("salesFilterUser");
        const expensesFilterUser =
          document.getElementById("expensesFilterUser");

        if (salesFilterUser) {
          const currentValue = salesFilterUser.value;
          salesFilterUser.innerHTML =
            '<option value="all">جميع المستخدمين</option>' +
            users
              .map(
                (user) => `<option value="${user.name}">${user.name}</option>`,
              )
              .join("");
          if (currentValue && currentValue !== "all")
            salesFilterUser.value = currentValue;
        }

        if (expensesFilterUser) {
          const currentValue = expensesFilterUser.value;
          expensesFilterUser.innerHTML =
            '<option value="all">جميع المستخدمين</option>' +
            users
              .map(
                (user) => `<option value="${user.name}">${user.name}</option>`,
              )
              .join("");
          if (currentValue && currentValue !== "all")
            expensesFilterUser.value = currentValue;
        }
      }

      async function addUser() {
        const username = document.getElementById("newUsername").value.trim();
        const fullName = document.getElementById("newFullName").value.trim();
        const password = document.getElementById("newPassword").value;
        const role = document.getElementById("newUserRole").value;

        if (!username || !fullName || !password) {
          showNotification("❌ يرجى ملء جميع الحقول", "error");
          return;
        }

        try {
          const users = await DataManager.getUsers();

          if (users.find((u) => u.username === username)) {
            showNotification("❌ اسم المستخدم موجود بالفعل", "error");
            return;
          }

          const newUser = {
            username: username,
            name: fullName,
            password: password,
            role: role,
            createdAt: new Date().toISOString(),
          };
          users.push(newUser);
          const result = await DataManager.saveUsers(users);

          if (result.success) {
            showNotification("✅ تم إضافة المستخدم بنجاح", "success");

            document.getElementById("newUsername").value = "";
            document.getElementById("newFullName").value = "";
            document.getElementById("newPassword").value = "";
            document.getElementById("newUserRole").value = "cashier";

            window.users = users;
            loadUsers();
            updateUserFilterOptions();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في إضافة المستخدم:", error);
          showNotification("❌ حدث خطأ في إضافة المستخدم", "error");
        }
      }

      async function deleteUser(username) {
        if (confirm("هل أنت متأكد من حذف هذا المستخدم؟")) {
          const users = await DataManager.getUsers();
          const updatedUsers = users.filter((u) => u.username !== username);
          const result = await DataManager.saveUsers(updatedUsers);
          if (result.success) {
            showNotification("✅ تم حذف المستخدم بنجاح", "success");
            loadUsers();
            updateUserFilterOptions();
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        }
      }

      function editUser(username) {
        showNotification("🔧 وظيفة تعديل المستخدم قيد التطوير", "info");
      }

      // ==================== دوال معلومات المطعم ====================
      async function loadRestaurantInfo() {
        try {
          restaurantInfo = await DataManager.getRestaurantInfo();
          if (!restaurantInfo.deliveryNumbers)
            restaurantInfo.deliveryNumbers = [];
          if (!restaurantInfo.deliveryPrices)
            restaurantInfo.deliveryPrices = [0, 0, 0, 0, 0, 0];

          document.getElementById("restaurantName").value =
            restaurantInfo.name || "";
          document.getElementById("restaurantNumber").value =
            restaurantInfo.number || "";
          document.getElementById("branchName").value =
            restaurantInfo.branchName || "";

          // NEW: load delivery prices
          for (let i = 0; i < 6; i++) {
            const input = document.getElementById(`zonePrice${i + 1}`);
            if (input) input.value = restaurantInfo.deliveryPrices[i] || 0;
          }

          updateDeliveryNumbersList();
        } catch (error) {
          console.error("❌ خطأ في تحميل معلومات المطعم:", error);
          showNotification("❌ حدث خطأ في تحميل معلومات المطعم", "error");
        }
      }

      async function saveRestaurantInfo() {
        restaurantInfo.name = document
          .getElementById("restaurantName")
          .value.trim();
        restaurantInfo.number = document
          .getElementById("restaurantNumber")
          .value.trim();
        restaurantInfo.branchName = document
          .getElementById("branchName")
          .value.trim();
        if (!restaurantInfo.deliveryNumbers)
          restaurantInfo.deliveryNumbers = [];

        // NEW: save delivery prices
        for (let i = 0; i < 6; i++) {
          const input = document.getElementById(`zonePrice${i + 1}`);
          restaurantInfo.deliveryPrices[i] = parseFloat(input.value) || 0;
        }

        try {
          const result = await DataManager.saveRestaurantInfo(restaurantInfo);
          if (result.success) {
            showNotification("✅ تم حفظ معلومات المطعم بنجاح", "success");
          } else {
            showNotification(`❌ ${result.message}`, "error");
          }
        } catch (error) {
          console.error("❌ خطأ في حفظ معلومات المطعم:", error);
          showNotification("❌ حدث خطأ في حفظ معلومات المطعم", "error");
        }
      }

      function updateDeliveryNumbersList() {
        const container = document.getElementById("deliveryNumbersList");

        if (
          !restaurantInfo.deliveryNumbers ||
          restaurantInfo.deliveryNumbers.length === 0
        ) {
          container.innerHTML = "<p>لا توجد أرقام توصيل حالياً</p>";
          return;
        }

        container.innerHTML = restaurantInfo.deliveryNumbers
          .map(
            (number, index) => `
            <div class="delivery-number-tag">
                ${number}
                <button onclick="deleteDeliveryNumber(${index})"><i class="fas fa-times"></i></button>
            </div>
        `,
          )
          .join("");
      }

      function addDeliveryNumber() {
        const newNumber = document
          .getElementById("newDeliveryNumber")
          .value.trim();

        if (!newNumber) {
          showNotification("❌ يرجى إدخال رقم التوصيل", "error");
          return;
        }

        if (!restaurantInfo.deliveryNumbers)
          restaurantInfo.deliveryNumbers = [];

        if (restaurantInfo.deliveryNumbers.includes(newNumber)) {
          showNotification("❌ رقم التوصيل موجود بالفعل", "error");
          return;
        }

        restaurantInfo.deliveryNumbers.push(newNumber);
        document.getElementById("newDeliveryNumber").value = "";
        updateDeliveryNumbersList();
        showNotification("✅ تم إضافة رقم التوصيل بنجاح", "success");
      }

      function addMultipleDeliveryNumbers() {
        const numbersText = document
          .getElementById("multipleDeliveryNumbers")
          .value.trim();

        if (!numbersText) {
          showNotification("❌ يرجى إدخال أرقام التوصيل", "error");
          return;
        }

        if (!restaurantInfo.deliveryNumbers)
          restaurantInfo.deliveryNumbers = [];

        const numbers = numbersText.split("\n").filter((n) => n.trim());

        if (numbers.length === 0) {
          showNotification("❌ لم يتم العثور على أرقام صالحة", "error");
          return;
        }

        let addedCount = 0,
          duplicateCount = 0;

        numbers.forEach((number) => {
          const trimmedNumber = number.trim();
          if (
            trimmedNumber &&
            !restaurantInfo.deliveryNumbers.includes(trimmedNumber)
          ) {
            restaurantInfo.deliveryNumbers.push(trimmedNumber);
            addedCount++;
          } else if (trimmedNumber) {
            duplicateCount++;
          }
        });

        document.getElementById("multipleDeliveryNumbers").value = "";
        updateDeliveryNumbersList();

        if (addedCount > 0)
          showNotification(
            `✅ تم إضافة ${addedCount} رقم توصيل بنجاح`,
            "success",
          );
        if (duplicateCount > 0)
          showNotification(
            `⚠️ ${duplicateCount} أرقام مكررة تم تجاهلها`,
            "warning",
          );
      }

      function deleteDeliveryNumber(index) {
        if (confirm("هل أنت متأكد من حذف هذا الرقم؟")) {
          if (!restaurantInfo.deliveryNumbers)
            restaurantInfo.deliveryNumbers = [];
          restaurantInfo.deliveryNumbers.splice(index, 1);
          updateDeliveryNumbersList();
          showNotification("✅ تم حذف رقم التوصيل بنجاح", "success");
        }
      }

      // ==================== دوال التبويبات ====================
      function switchAdminTab(tabName, event) {
        if (event) event.preventDefault();

        document
          .querySelectorAll("#adminScreen .tab-content")
          .forEach((content) => {
            content.classList.remove("active");
            content.style.display = "none";
          });

        document.querySelectorAll("#adminScreen .tab-btn").forEach((button) => {
          button.classList.remove("active");
        });

        const selectedTab = document.getElementById(tabName + "Tab");
        if (selectedTab) {
          selectedTab.classList.add("active");
          selectedTab.style.display = "block";
        }

        if (event?.currentTarget) {
          event.currentTarget.classList.add("active");
        }

        switch (tabName) {
          case "dashboard":
            if (typeof updateDashboard === "function") updateDashboard();
            break;
          case "products":
            if (typeof loadAdminProducts === "function") loadAdminProducts();
            break;
          case "productSales":
            if (typeof loadProductSales === "function") {
              const today = new Date().toISOString().split("T")[0];
              const startDate = document.getElementById(
                "productSalesStartDate",
              );
              const endDate = document.getElementById("productSalesEndDate");
              if (startDate) startDate.value = today;
              if (endDate) endDate.value = today;
              loadProductSales();
            }
            break;
          case "sales":
            if (typeof loadAdminSales === "function") {
              const today = new Date().toISOString().split("T")[0];
              const startDate = document.getElementById("salesFilterStartDate");
              const endDate = document.getElementById("salesFilterEndDate");
              if (startDate) startDate.value = today;
              if (endDate) endDate.value = today;
              loadAdminSales();
            }
            break;
          case "delivery":
            if (typeof loadAdminDeliveryData === "function")
              loadAdminDeliveryData();
            break;
          case "expenses":
            if (typeof loadExpenses === "function") {
              const today = new Date().toISOString().split("T")[0];
              const startDate = document.getElementById(
                "expensesFilterStartDate",
              );
              const endDate = document.getElementById("expensesFilterEndDate");
              if (startDate) startDate.value = today;
              if (endDate) endDate.value = today;
              loadExpenses();
            }
            break;
          case "categories":
            if (typeof loadCategories === "function") loadCategories();
            break;
          case "employees":
            if (typeof loadEmployees === "function") loadEmployees();
            break;
          case "users":
            if (typeof loadUsers === "function") loadUsers();
            break;
          case "restaurantInfo":
            if (typeof loadRestaurantInfo === "function") loadRestaurantInfo();
            break;
        }
      }

      function switchCashierTab(tab) {
        document
          .querySelectorAll("#cashierScreen .tab-btn")
          .forEach((btn) => btn.classList.remove("active"));
        if (event?.currentTarget) event.currentTarget.classList.add("active");

        document
          .querySelectorAll("#cashierScreen .tab-content")
          .forEach((content) => {
            content.classList.remove("active");
            content.style.display = "none";
          });

        let tabId = "";
        if (tab === "pos") tabId = "cashierPosTab";
        else if (tab === "reports") tabId = "cashierReportsTab";
        else if (tab === "delivery") tabId = "cashierDeliveryTab";

        const selectedTab = document.getElementById(tabId);
        if (selectedTab) {
          selectedTab.classList.add("active");
          selectedTab.style.display = "block";
        }

        if (tab === "reports") {
          // تعيين تاريخ اليوم في حقلي التاريخ قبل تحميل التقرير
          const today = new Date().toISOString().split("T")[0];
          document.getElementById("cashierFilterStartDate").value = today;
          document.getElementById("cashierFilterEndDate").value = today;
          loadCashierReport();
        } else if (tab === "delivery") {
          loadUserDeliveryData();
        }
      }
      // ==================== دوال الطباعة والتصدير ====================
      function exportCashierReportToExcel() {
        try {
          const table = document.getElementById(
            "cashierReportTableBody",
          ).parentElement;
          if (!table || table.rows.length <= 1) {
            showNotification("❌ لا توجد بيانات للتصدير", "error");
            return;
          }

          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "تقرير_الكاشير");
          XLSX.writeFile(
            wb,
            `تقرير_الكاشير_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير التقرير إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification("❌ حدث خطأ أثناء التصدير إلى Excel", "error");
        }
      }

      function exportProductsToExcel() {
        try {
          const table =
            document.getElementById("productsTableBody").parentElement;
          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المنتجات");
          XLSX.writeFile(
            wb,
            `المنتجات_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير المنتجات إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير المنتجات:", error);
          showNotification("❌ حدث خطأ أثناء تصدير المنتجات", "error");
        }
      }

      function exportAdminSalesToExcel() {
        try {
          const table = document.getElementById("salesTableBody").parentElement;
          if (!table || table.rows.length <= 1) {
            showNotification("❌ لا توجد بيانات للتصدير", "error");
            return;
          }

          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المبيعات");
          XLSX.writeFile(
            wb,
            `المبيعات_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير المبيعات إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير المبيعات:", error);
          showNotification("❌ حدث خطأ أثناء تصدير المبيعات", "error");
        }
      }

      function exportExpensesToExcel() {
        try {
          const table =
            document.getElementById("expensesTableBody").parentElement;
          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المصاريف");
          XLSX.writeFile(
            wb,
            `المصاريف_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير المصاريف إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير المصاريف:", error);
          showNotification("❌ حدث خطأ أثناء تصدير المصاريف", "error");
        }
      }

      function exportProductSalesToExcel() {
        try {
          const table = document.getElementById(
            "productSalesTableBody",
          ).parentElement;
          const ws = XLSX.utils.table_to_sheet(table);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "مبيعات_المنتجات");
          XLSX.writeFile(
            wb,
            `مبيعات_المنتجات_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification(
            "✅ تم تصدير مبيعات المنتجات إلى Excel بنجاح",
            "success",
          );
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification("❌ حدث خطأ أثناء التصدير إلى Excel", "error");
        }
      }

      function printProducts() {
        const printWindow = window.open("", "", "width=800,height=600");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head><style>
                body { font-family: Arial; padding: 20px; }
                h2 { text-align: center; }
                .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                table { width: 100%; border-collapse: collapse; margin: 10px 0; }
                th, td { border: 1px solid #000; padding: 8px; text-align: center; }
                .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
                .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
            </style></head>
            <body>
                <div class="watermark">amaryasser408@gmail.com</div>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                </div>
                <h3>قائمة المنتجات</h3>
                <h4>المستخدم: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                <table><thead><tr><th>الصورة</th><th>الاسم</th><th>السعر</th><th>القسم</th><th>المكونات</th></tr></thead>
                <tbody>${document.getElementById("productsTableBody").innerHTML}</tbody></table>
                <div class="signature-section">
                    <div class="signature-box"><p>المدير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                    <div class="signature-box"><p>التوقيع</p><p>....................</p></div>
                </div>
            </body></html>
        `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      function printProductSales() {
        const printWindow = window.open("", "", "width=800,height=600");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head><style>
                body { font-family: Arial; padding: 20px; }
                h2, h3 { text-align: center; }
                .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                table { width: 100%; border-collapse: collapse; margin: 10px 0; }
                th, td { border: 1px solid #000; padding: 8px; text-align: right; }
                .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
                .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
            </style></head>
            <body>
                <div class="watermark">amaryasser408@gmail.com</div>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                </div>
                <h3>تقرير مبيعات المنتجات والمكونات</h3>
                <h4>المستخدم: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                <table><thead><tr><th>اسم المنتج</th><th>عدد مرات البيع</th><th>إجمالي الكمية</th><th>إجمالي المبيعات</th><th>المكونات المستهلكة</th></tr></thead>
                <tbody>${document.getElementById("productSalesTableBody").innerHTML}</tbody></table>
                <div class="signature-section">
                    <div class="signature-box"><p>المدير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                    <div class="signature-box"><p>التوقيع</p><p>....................</p></div>
                </div>
            </body></html>
        `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      function printCategories() {
        const printWindow = window.open("", "", "width=800,height=600");
        const html = `
            <!DOCTYPE html>
            <html dir="rtl">
            <head><style>
                body { font-family: Arial; padding: 20px; }
                h2, h3 { text-align: center; }
                .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                .categories-list { display: flex; flex-wrap: wrap; gap: 15px; margin: 20px 0; justify-content: center; }
                .category-item { background: #f9f9f9; border: 2px solid var(--primary-color); border-radius: 10px; padding: 15px 20px; min-width: 150px; text-align: center; }
                .category-name { font-weight: bold; font-size: 16px; color: var(--secondary-color); }
                .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
                .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
            </style></head>
            <body>
                <div class="watermark">amaryasser408@gmail.com</div>
                <div style="text-align: center;">
                    <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                    <h2>🍖 ${restaurantInfo.name}</h2>
                    <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                </div>
                <h3>قائمة الأقسام</h3>
                <h4>المستخدم: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                <div class="categories-list">
                    ${categories
                      .map(
                        (category) => `
                        <div class="category-item">
                            <div class="category-name">${category.name}</div>
                            <div class="category-id">رمز القسم: ${category.id}</div>
                        </div>
                    `,
                      )
                      .join("")}
                </div>
                <div class="signature-section">
                    <div class="signature-box"><p>المدير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                    <div class="signature-box"><p>التوقيع</p><p>....................</p></div>
                </div>
            </body></html>
        `;
        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      function exportCategoriesToExcel() {
        try {
          const data = [];
          data.push(["قائمة الأقسام", "", ""]);
          data.push(["المطعم:", restaurantInfo.name, ""]);
          data.push([
            "الفرع:",
            `${restaurantInfo.number} - ${restaurantInfo.branchName}`,
            "",
          ]);
          data.push(["التاريخ:", new Date().toLocaleDateString("ar-EG"), ""]);
          data.push([
            "المستخدم:",
            currentUser ? currentUser.name : "غير محدد",
            "",
          ]);
          data.push([]);
          data.push(["اسم القسم", "رمز القسم", "عدد المنتجات"]);

          categories.forEach((category) => {
            const productCount = products.filter(
              (p) => p.category === category.id,
            ).length;
            data.push([category.name, category.id, productCount]);
          });

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "الأقسام");
          XLSX.writeFile(
            wb,
            `قائمة_الأقسام_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير الأقسام إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification("❌ حدث خطأ أثناء تصدير الأقسام إلى Excel", "error");
        }
      }

      async function printUsers() {
        try {
          let usersList = users || (await DataManager.getUsers());
          const printWindow = window.open("", "", "width=800,height=600");
          const html = `
                <!DOCTYPE html>
                <html dir="rtl">
                <head><style>
                    body { font-family: Arial; padding: 20px; }
                    h2, h3 { text-align: center; }
                    .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; border: 2px solid #ddd; }
                    table { width: 100%; border-collapse: collapse; margin: 10px 0; }
                    th, td { border: 1px solid #000; padding: 8px; text-align: center; }
                    .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
                    .signature-section { display: flex; justify-content: space-between; margin-top: 40px; }
                    .signature-box { width: 45%; text-align: center; border-top: 1px solid #000; padding-top: 10px; }
                </style></head>
                <body>
                    <div class="watermark">amaryasser408@gmail.com</div>
                    <div style="text-align: center;">
                        <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                        <h2>🍖 ${restaurantInfo.name}</h2>
                        <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
                    </div>
                    <h3>قائمة المستخدمين</h3>
                    <h4>المستخدم: ${currentUser ? currentUser.name : "غير محدد"}</h4>
                    <table><thead><tr><th>اسم المستخدم</th><th>الاسم الكامل</th><th>الدور</th></tr></thead>
                    <tbody>${usersList.map((user) => `<tr><td>${user.username}</td><td>${user.name}</td><td>${user.role === "admin" ? "مدير" : "كاشير"}</td></tr>`).join("")}</tbody></table>
                    <div class="signature-section">
                        <div class="signature-box"><p>المدير</p><p>${currentUser ? currentUser.name : "...................."}</p></div>
                        <div class="signature-box"><p>التوقيع</p><p>....................</p></div>
                    </div>
                </body></html>
            `;
          printWindow.document.write(html);
          printWindow.document.close();
          printWindow.print();
        } catch (error) {
          console.error("❌ خطأ في طباعة المستخدمين:", error);
          showNotification("❌ حدث خطأ أثناء طباعة المستخدمين", "error");
        }
      }

      async function exportUsersToExcel() {
        try {
          let usersList = users || (await DataManager.getUsers());
          const data = [];
          data.push(["قائمة المستخدمين", "", ""]);
          data.push(["المطعم:", restaurantInfo.name, ""]);
          data.push([
            "الفرع:",
            `${restaurantInfo.number} - ${restaurantInfo.branchName}`,
            "",
          ]);
          data.push(["التاريخ:", new Date().toLocaleDateString("ar-EG"), ""]);
          data.push([
            "المستخدم:",
            currentUser ? currentUser.name : "غير محدد",
            "",
          ]);
          data.push([]);
          data.push(["اسم المستخدم", "الاسم الكامل", "الدور"]);

          usersList.forEach((user) => {
            data.push([
              user.username,
              user.name,
              user.role === "admin" ? "مدير" : "كاشير",
            ]);
          });

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المستخدمون");
          XLSX.writeFile(
            wb,
            `قائمة_المستخدمين_${new Date().toISOString().split("T")[0]}.xlsx`,
          );
          showNotification("✅ تم تصدير المستخدمين إلى Excel بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير Excel:", error);
          showNotification(
            "❌ حدث خطأ أثناء تصدير المستخدمين إلى Excel",
            "error",
          );
        }
      }

      function printSingleDeliveryInvoice(orderId) {
        const order = deliveryOrders.find((o) => o.id === orderId);
        if (!order) {
          showNotification("❌ لم يتم العثور على الطلب", "error");
          return;
        }

        const personnelInput = document.getElementById(
          `personnel-name-${orderId}`,
        );
        if (personnelInput && personnelInput.value.trim()) {
          order.deliveryPersonnelName = personnelInput.value.trim();
          localStorage.setItem(
            "kafta_delivery_orders",
            JSON.stringify(deliveryOrders),
          );
        }

        showPrintModal(order);
      }

      // ==================== دوال الطباعة المتقدمة ====================
      function showPrintModal(sale) {
        try {
          // إزالة أي iframe سابق
          const oldIframe = document.getElementById("print-iframe");
          if (oldIframe && oldIframe.parentNode) {
            oldIframe.parentNode.removeChild(oldIframe);
          }

          const orderTypeNames = {
            hall: "صالة",
            takeout: "تيك أوت",
            delivery: "توصيل",
          };

          const styles = `
    <style>
      @page { size: 72mm auto; margin: 2mm; }
      body { font-family: Tahoma, Arial; font-size: 12px; margin: 0; padding: 0; width: 72mm; color: #000; background: #fff; }
      .receipt { padding: 3px; margin: 0; width: 100%; box-sizing: border-box; text-align: center; }
      .store-name { font-size: 16px; font-weight: bold; margin: 2px 0; }
      .copy-title { font-size: 14px; font-weight: bold; margin-bottom: 3px; background: #f0f0f0; padding: 3px 0; }
      .logo { width: 100px; height: 100px; display: block; margin: 3px auto; }
      .order-type { font-size: 13px; font-weight: bold; margin: 3px 0; border: 1px solid #000; display: inline-block; padding: 2px 8px; }
      .divider { border-top: 1px dashed #000; margin: 4px 0; }
      .info { text-align: center; font-size: 11px; padding: 0 3px; }
      .item-table { width: 100%; border-collapse: collapse; font-size: 11px; border: 1px solid #000; }
      .item-table th, .item-table td { border: 1px solid #000; padding: 4px; text-align: center; }
      .total { font-size: 13px; font-weight: bold; margin-top: 3px; }
      .footer { font-size: 11px; margin-top: 5px; font-weight: bold; }
      .watermark { font-size: 9px; opacity: 0.6; margin-top: 5px; }
      
      /* تنسيق خاص بفاتورة الدليفري */
      .delivery-receipt {
        background: #fff;
        border: 2px solid #000;
        border-radius: 5px;
        padding: 8px;
      }
      .delivery-receipt .copy-title {
        background: #000;
        color: #fff;
        border-radius: 20px;
        padding: 6px;
      }
      .delivery-info-box {
        background: #f9f9f9;
        border: 1px solid #000;
        border-radius: 5px;
        padding: 8px;
        margin: 8px 0;
        text-align: right;
        color: #000;
      }
      .delivery-info-box p {
        margin: 5px 0;
        font-size: 11px;
        color: #000;
      }
      .delivery-info-box strong {
        color: #000;
      }
    </style>
  `;

          // إنشاء HTML لفاتورة الدليفري بشكل منفصل ومميز
          const deliveryReceiptHTML =
            sale.orderType === "delivery"
              ? `
    <div style="page-break-after: always;"></div>
    <div class="receipt delivery-receipt">
      <div class="copy-title">🚚 فاتورة التوصيل</div>
      <!-- تم إزالة الصورة -->
      <div class="store-name">${restaurantInfo?.name || "كفتة على الفحم"}</div>
      <div class="store-info">رقم الفرع: ${restaurantInfo?.number || "1"} - ${restaurantInfo?.branchName || "الفرع الرئيسي"}</div>
      
      <div class="delivery-info-box">
        <p><strong>🧾 رقم الفاتورة:</strong> ${String(sale.invoiceNumber).padStart(4, "0")}</p>
        <p><strong>👤 العميل:</strong> ${sale.customerName || "غير محدد"}</p>
        <p><strong>📞 رقم التوصيل:</strong> ${sale.deliveryNumber || "-"}</p>
        <p><strong>📍 عنوان التوصيل:</strong> ${sale.deliveryLocation || "-"}</p>
        ${sale.deliveryZone ? `<p><strong>🗺️ منطقة التوصيل:</strong> ${sale.deliveryZone}</p>` : ""}
        <p><strong>🛵 الموصل:</strong> ${sale.deliveryPersonnelName || "لم يُعين بعد"}</p>
        <p><strong>💳 طريقة الدفع:</strong> ${getDeliveryPaymentMethodName(sale.deliveryPaymentMethod) || "غير محدد"}</p>
        <p><strong>⏱️ حالة الطلب:</strong> ${sale.status === "delivered" ? "تم التوصيل" : "قيد التوصيل"}</p>
        ${sale.deliveredAt ? `<p><strong>✅ تم التوصيل في:</strong> ${new Date(sale.deliveredAt).toLocaleString("en-GB")}</p>` : ""}
      </div>

      <div class="divider"></div>
      <div class="items">
        <table class="item-table">
          <thead><tr><th>الصنف</th><th>الكمية</th><th>السعر</th><th>الإجمالي</th></tr></thead>
          <tbody>${sale.items
            .map(
              (i) => `
            <tr>
              <td>${i.name}</td>
              <td>${i.quantity}</td>
              <td>${(i.price || 0).toFixed(2)}</td>
              <td>${((i.price || 0) * i.quantity).toFixed(2)}</td>
            </tr>`,
            )
            .join("")}
          </tbody>
        </table>
      </div>
      
      ${sale.orderNotes ? `<div class="notes"><strong>ملاحظات:</strong> ${sale.orderNotes}</div>` : ""}
      
      <div class="totals-container">
        ${sale.discount > 0 ? `<div class="discount">الخصم: -${sale.discount.toFixed(2)} ج.م</div>` : ""}
        <div class="total">💰 الإجمالي المطلوب: ${sale.finalTotal.toFixed(2)} ج.م</div>
      </div>

      <!-- تم إزالة قسم التوقيع -->

      <div class="footer">شكراً لتعاملكم معنا 🤍</div>
      <div class="watermark">Delivery Receipt</div>
    </div>
  `
              : "";

          const html = `
    <!DOCTYPE html>
    <html dir="rtl">
    <head>
      <meta charset="UTF-8">
      <meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
      <meta http-equiv="Pragma" content="no-cache">
      <meta http-equiv="Expires" content="0">
      ${styles}
    </head>
    <body>
      <!-- نسخة المطبخ -->
      <div class="receipt">
        <div class="copy-title">🍳 مطبخ</div>
        <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="logo">
        <div class="store-name">${restaurantInfo?.name || "كفتة على الفحم"}</div>
        <div class="order-type">${orderTypeNames[sale.orderType]}</div>
        ${sale.tableNumber ? `<div class="order-type">طاولة: ${sale.tableNumber}</div>` : ""}
        <div class="info">
          <div>طلب رقم: <strong>${String(sale.invoiceNumber).padStart(4, "0")}</strong></div>
          <div>${new Date(sale.date).toLocaleDateString("en-GB")} - ${new Date(sale.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</div>
        </div>
        <div class="divider"></div>
        <div class="items">
          <table class="item-table">
            <thead><tr><th>الصنف</th><th>الكمية</th></tr></thead>
            <tbody>${sale.items.map((i) => `<tr><td>${i.name}</td><td>${i.quantity}</td></tr>`).join("")}</tbody>
          </table>
        </div>
        ${sale.orderNotes ? `<div class="notes">ملاحظات: ${sale.orderNotes}</div>` : ""}
        <div class="divider"></div>
        <div class="watermark">Kitchen</div>
      </div>
      
      <div style="page-break-after: always;"></div>
      
      <!-- نسخة العميل -->
      <div class="receipt">
        <div class="copy-title">🧾 فاتورة العميل</div>
        <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="logo">
        <div class="store-name">${restaurantInfo?.name || "كفتة على الفحم"}</div>
        <div class="store-info">رقم الفرع: ${restaurantInfo?.number || "1"} - ${restaurantInfo?.branchName || "الفرع الرئيسي"}</div>
        <div class="order-type">${orderTypeNames[sale.orderType]}</div>
        ${sale.tableNumber ? `<div class="order-type">طاولة: ${sale.tableNumber}</div>` : ""}
        <div class="info">
          <div>فاتورة رقم: <strong>${String(sale.invoiceNumber).padStart(4, "0")}</strong></div>
          <div>${new Date(sale.date).toLocaleDateString("en-GB")} - ${new Date(sale.date).toLocaleTimeString("en-US", { hour: "2-digit", minute: "2-digit" })}</div>
          ${sale.customerName ? `<div>العميل: ${sale.customerName}</div>` : ""}
          ${sale.deliveryNumber ? `<div>رقم التوصيل: ${sale.deliveryNumber}</div>` : ""}
          ${sale.deliveryLocation ? `<div>مكان التوصيل: ${sale.deliveryLocation}</div>` : ""}
          ${sale.deliveryZone ? `<div>منطقة التوصيل: ${sale.deliveryZone} (${sale.deliveryPrice} ج)</div>` : ""}
        </div>
        <div class="divider"></div>
        <div class="items">
          <table class="item-table">
            <thead><tr><th>الصنف</th><th>الكمية</th><th>السعر</th><th>الإجمالي</th></tr></thead>
            <tbody>${sale.items
              .map(
                (i) => `
              <tr>
                <td>${i.name}</td>
                <td>${i.quantity}</td>
                <td>${(i.price || 0).toFixed(2)}</td>
                <td>${((i.price || 0) * i.quantity).toFixed(2)}</td>
              </tr>`,
              )
              .join("")}
            </tbody>
          </table>
        </div>
        ${sale.orderNotes ? `<div class="notes">ملاحظات: ${sale.orderNotes}</div>` : ""}
        <div class="divider"></div>
        <div class="totals-container">
          ${sale.discount > 0 ? `<div class="discount">الخصم: -${sale.discount.toFixed(2)} ج.م</div>` : ""}
          <div class="total">الإجمالي النهائي: ${sale.finalTotal.toFixed(2)} ج.م</div>
        </div>
        <div class="info">طريقة الدفع: <strong>${getPaymentMethodName(sale.paymentMethod)}</strong></div>
        ${
          restaurantInfo?.deliveryNumbers?.length
            ? `
          <div class="contact-info">أرقام التوصيل: ${restaurantInfo.deliveryNumbers.map((num) => `<div>${num}</div>`).join("")}</div>
        `
            : ""
        }
        <div class="footer">شكراً لزيارتكم 🤍</div>
        <div class="watermark">Xprinter • Receipt</div>
      </div>
      
      ${deliveryReceiptHTML}
    </body></html>
  `;

          // إنشاء iframe جديد
          const iframe = document.createElement("iframe");
          iframe.id = "print-iframe";
          iframe.style.position = "absolute";
          iframe.style.width = "0";
          iframe.style.height = "0";
          iframe.style.border = "none";
          iframe.style.visibility = "hidden";
          document.body.appendChild(iframe);

          const iframeDoc = iframe.contentWindow.document;
          iframeDoc.open();
          iframeDoc.write(html);
          iframeDoc.close();

          setTimeout(() => {
            try {
              iframe.contentWindow.focus();
              iframe.contentWindow.print();

              // إزالة iframe بعد الطباعة
              iframe.contentWindow.onafterprint = function () {
                setTimeout(() => {
                  if (iframe.parentNode) {
                    document.body.removeChild(iframe);
                  }
                }, 500);
              };
            } catch (error) {
              console.error("❌ فشلت الطباعة:", error);
              showNotification("❌ حدث خطأ في الطباعة", "error");
              if (iframe.parentNode) {
                document.body.removeChild(iframe);
              }
            }
          }, 300);
        } catch (error) {
          console.error("❌ خطأ في showPrintModal:", error);
          showNotification("❌ حدث خطأ في تجهيز الفاتورة للطباعة", "error");
        }
      }

      function printSingleInvoice(saleId) {
        const sale = sales.find((s) => s.id === saleId);
        if (sale) showPrintModal(sale);
      }

      function togglePasswordVisibility() {
        const passwordInput = document.getElementById("password");
        const toggleIcon = document.getElementById("togglePassword");

        if (passwordInput.type === "password") {
          passwordInput.type = "text";
          toggleIcon.classList.remove("fa-eye");
          toggleIcon.classList.add("fa-eye-slash");
          toggleIcon.style.color = "var(--secondary-color)";
        } else {
          passwordInput.type = "password";
          toggleIcon.classList.remove("fa-eye-slash");
          toggleIcon.classList.add("fa-eye");
          toggleIcon.style.color = "#666";
        }
      }

      // ==================== التهيئة عند تحميل الصفحة ====================
      document.addEventListener("DOMContentLoaded", () => {
        const today = new Date().toISOString().split("T")[0];

        const expenseDateInput = document.getElementById("expenseDate");
        if (expenseDateInput) {
          expenseDateInput.value = today;
          expenseDateInput.max = today;
        }

        const employeeHireDate = document.getElementById("employeeHireDate");
        if (employeeHireDate) {
          employeeHireDate.value = today;
          employeeHireDate.max = today;
        }

        const cashierStartDate = document.getElementById(
          "cashierFilterStartDate",
        );
        const cashierEndDate = document.getElementById("cashierFilterEndDate");
        if (cashierStartDate && cashierEndDate) {
          cashierStartDate.value = today;
          cashierEndDate.value = today;
          cashierStartDate.max = today;
          cashierEndDate.max = today;
        }

        const salesStartDate = document.getElementById("salesFilterStartDate");
        const salesEndDate = document.getElementById("salesFilterEndDate");
        if (salesStartDate && salesEndDate) {
          salesStartDate.value = today;
          salesEndDate.value = today;
        }

        const expensesStartDate = document.getElementById(
          "expensesFilterStartDate",
        );
        const expensesEndDate = document.getElementById(
          "expensesFilterEndDate",
        );
        if (expensesStartDate && expensesEndDate) {
          expensesStartDate.value = today;
          expensesEndDate.value = today;
        }

        const productSalesStartDate = document.getElementById(
          "productSalesStartDate",
        );
        const productSalesEndDate = document.getElementById(
          "productSalesEndDate",
        );
        if (productSalesStartDate && productSalesEndDate) {
          productSalesStartDate.value = today;
          productSalesEndDate.value = today;
        }

        ["userDeliveryPersonnel", "adminDeliveryPersonnel"].forEach((id) => {
          const select = document.getElementById(id);
          if (select)
            select.innerHTML = '<option value="all">جميع الموصلين</option>';
        });

        try {
          const savedDeliveryOrders = localStorage.getItem(
            "kafta_delivery_orders",
          );
          if (savedDeliveryOrders)
            deliveryOrders = JSON.parse(savedDeliveryOrders);

          const savedPersonnel = localStorage.getItem(
            "kafta_delivery_personnel",
          );
          if (savedPersonnel) deliveryPersonnel = JSON.parse(savedPersonnel);
        } catch (error) {
          console.error("❌ خطأ في تحميل بيانات الدليفري:", error);
        }

        window.addEventListener("online", () => updateConnectionStatus(true));
        window.addEventListener("offline", () => updateConnectionStatus(false));

        SyncManager.init();
        updateConnectionStatus(navigator.onLine);
      });

      window.addEventListener("userDataUpdated", () => {
        updateUserFilterOptions();
      });

      console.log("✅ تم تحميل جميع الدوال بنجاح!");

      // ==================== نظام المرتجعات (خاص بالمدير فقط) ====================

      let returns = []; // مصفوفة المرتجعات

      // تحميل المرتجعات من Firebase
      async function loadReturns() {
        try {
          const doc = await db.collection("returns").doc("all_returns").get();
          returns = doc.exists ? doc.data().data : [];
        } catch (error) {
          console.error("❌ خطأ في تحميل المرتجعات:", error);
          returns = [];
        }
      }

      // حفظ المرتجعات في Firebase
      async function saveReturns() {
        try {
          await db
            .collection("returns")
            .doc("all_returns")
            .set({
              data: returns,
              lastUpdated: new Date().toISOString(),
              totalAmount: returns.reduce((sum, r) => sum + r.amount, 0),
            });
          return { success: true };
        } catch (error) {
          console.error("❌ خطأ في حفظ المرتجعات:", error);
          return { success: false, error: error.message };
        }
      }

      // تحديث إحصائيات اليوم بعد الإرجاع
      function updateTodayStatsAfterReturn(returnAmount) {
        // تحديث إحصائيات اليوم في الكاشير
        const todaySalesAmount = document.getElementById("todaySalesAmount");
        if (todaySalesAmount) {
          let currentAmount = parseFloat(todaySalesAmount.textContent) || 0;
          currentAmount -= returnAmount;
          todaySalesAmount.textContent = currentAmount.toFixed(2) + " جنيه";
        }

        // تحديث صافي الدخل
        const todayNetAmount = document.getElementById("todayNetAmount");
        const todayExpensesAmount = document.getElementById(
          "todayExpensesAmount",
        );
        if (todayNetAmount && todayExpensesAmount) {
          let expenses = parseFloat(todayExpensesAmount.textContent) || 0;
          let sales = parseFloat(todaySalesAmount?.textContent) || 0;
          let net = sales - expenses;
          todayNetAmount.textContent = net.toFixed(2) + " جنيه";
        }

        // تحديث لوحة تحكم المدير إذا كانت مفتوحة
        if (document.getElementById("dashboardTotalSales")) {
          updateDashboard();
        }
      }

      // فتح نافذة إرجاع فاتورة (بحجم أصغر)
      function openReturnModal() {
        if (currentUser?.role !== "admin") {
          showNotification("❌ هذه الخاصية متاحة للمدير فقط", "error");
          return;
        }

        const modal = document.createElement("div");
        modal.className = "quantity-modal-overlay";
        modal.style.display = "flex";
        modal.innerHTML = `
        <div class="quantity-modal" style="max-width: 400px; width: 90%;">
            <div class="quantity-modal-header" style="padding: 12px;">
                <button class="quantity-modal-close" onclick="this.closest('.quantity-modal-overlay').remove()">
                    <i class="fas fa-times"></i>
                </button>
                <div class="quantity-modal-product" style="font-size: 16px;">
                    <i class="fas fa-undo-alt"></i>
                    إرجاع فاتورة
                </div>
                <div class="quantity-modal-price" style="font-size: 12px;">خاص بالمدير فقط</div>
            </div>
            <div class="quantity-display" style="padding: 15px; max-height: 70vh; overflow-y: auto;">
                <div class="form-group" style="margin-bottom: 12px;">
                    <label style="font-size: 13px;">🔍 رقم الفاتورة</label>
                    <input type="text" id="returnInvoiceNumber" placeholder="مثال: 0001 أو 1" style="font-size: 16px; text-align: center; padding: 10px;">
                </div>
                <div id="returnInvoicePreview" style="margin-top: 12px; display: none;">
                    <div style="background: #f0f8ff; padding: 12px; border-radius: 6px; font-size: 13px;">
                        <h4 style="color: var(--secondary-color); margin-bottom: 8px; font-size: 14px;">تفاصيل الفاتورة:</h4>
                        <div id="returnInvoiceDetails"></div>
                    </div>
                    <div class="form-group" style="margin-top: 12px;">
                        <label style="font-size: 13px;">✏️ سبب الإرجاع</label>
                        <textarea id="returnReason" placeholder="أدخل سبب الإرجاع" rows="2" style="width: 100%; padding: 8px; border-radius: 6px; font-size: 13px;"></textarea>
                    </div>
                </div>
            </div>
            <div class="quantity-keypad" style="padding: 12px;">
                <div class="quantity-action-buttons" style="gap: 8px;">
                    <button class="quantity-action-btn quantity-cancel-btn" onclick="this.closest('.quantity-modal-overlay').remove()" style="padding: 10px; font-size: 14px;">
                        <i class="fas fa-times"></i> إلغاء
                    </button>
                    <button class="quantity-action-btn quantity-add-btn" onclick="searchInvoiceForReturn()" id="searchInvoiceBtn" style="padding: 10px; font-size: 14px;">
                        <i class="fas fa-search"></i> بحث
                    </button>
                    <button class="quantity-action-btn quantity-add-btn" onclick="confirmReturn()" id="confirmReturnBtn" style="background: #f44336; display: none; padding: 10px; font-size: 14px;">
                        <i class="fas fa-check"></i> تأكيد
                    </button>
                </div>
            </div>
        </div>
    `;
        document.body.appendChild(modal);

        document.getElementById("returnInvoiceNumber").focus();
      }

      // البحث عن فاتورة للإرجاع
      function searchInvoiceForReturn() {
        const invoiceNumber = document
          .getElementById("returnInvoiceNumber")
          .value.trim();

        if (!invoiceNumber) {
          showNotification("❌ يرجى إدخال رقم الفاتورة", "error");
          return;
        }

        // تنظيف رقم الفاتورة من الأصفار البادئة
        const cleanNumber = invoiceNumber.replace(/^0+/, "");

        // البحث في المبيعات
        const sale = sales.find(
          (s) =>
            s.invoiceNumber == invoiceNumber ||
            s.invoiceNumber == cleanNumber ||
            String(s.invoiceNumber).padStart(4, "0") === invoiceNumber ||
            String(s.invoiceNumber) === invoiceNumber,
        );

        if (!sale) {
          showNotification("❌ لم يتم العثور على الفاتورة", "error");
          return;
        }

        // التحقق إذا كانت الفاتورة مرتجعة مسبقاً
        const existingReturn = returns.find(
          (r) => r.invoiceNumber == sale.invoiceNumber,
        );
        if (existingReturn) {
          showNotification("❌ هذه الفاتورة مرتجعة مسبقاً", "error");
          return;
        }

        // عرض تفاصيل الفاتورة (مصغرة)
        const previewDiv = document.getElementById("returnInvoicePreview");
        const detailsDiv = document.getElementById("returnInvoiceDetails");

        const orderTypeNames = {
          hall: "صالة",
          takeout: "تيك أوت",
          delivery: "توصيل",
        };
        const paymentMethodNames = {
          cash: "كاش",
          bank: "بنكك",
          foori: "فوري",
          okash: "أوكاش",
          sahel: "ساهل",
        };

        detailsDiv.innerHTML = `
        <div style="border-bottom: 1px solid #ddd; padding-bottom: 8px; margin-bottom: 8px; font-size: 12px;">
            <p style="margin: 3px 0;"><strong>رقم الفاتورة:</strong> ${String(sale.invoiceNumber).padStart(4, "0")}</p>
            <p style="margin: 3px 0;"><strong>التاريخ:</strong> ${new Date(sale.date).toLocaleDateString("ar-EG")}</p>
            <p style="margin: 3px 0;"><strong>الكاشير:</strong> ${sale.cashier}</p>
            <p style="margin: 3px 0;"><strong>طريقة الدفع:</strong> ${paymentMethodNames[sale.paymentMethod] || sale.paymentMethod}</p>
        </div>
        <div style="max-height: 150px; overflow-y: auto; margin-bottom: 8px;">
            <h5 style="font-size: 12px; margin: 5px 0;">المنتجات:</h5>
            ${sale.items
              .map(
                (item) => `
                <div style="display: flex; justify-content: space-between; padding: 3px 0; font-size: 11px;">
                    <span>${item.name} x${item.quantity}</span>
                    <span>${(item.price * item.quantity).toFixed(2)} ج</span>
                </div>
            `,
              )
              .join("")}
        </div>
        <div style="border-top: 1px solid var(--secondary-color); margin-top: 8px; padding-top: 8px;">
            <p style="font-size: 14px; color: var(--secondary-color); margin: 0; text-align: left;">
                <strong>المبلغ المسترد: ${sale.finalTotal.toFixed(2)} ج.م</strong>
            </p>
        </div>
    `;

        previewDiv.style.display = "block";
        document.getElementById("searchInvoiceBtn").style.display = "none";
        document.getElementById("confirmReturnBtn").style.display = "block";
        document.getElementById("returnInvoiceNumber").disabled = true;

        // حفظ بيانات الفاتورة للاستخدام لاحقاً
        window.currentReturnSale = sale;
      }

      // تأكيد عملية الإرجاع
      async function confirmReturn() {
        if (!window.currentReturnSale) {
          showNotification("❌ حدث خطأ، يرجى المحاولة مرة أخرى", "error");
          return;
        }

        const reason = document.getElementById("returnReason").value.trim();
        if (!reason) {
          showNotification("❌ يرجى إدخال سبب الإرجاع", "error");
          return;
        }

        if (
          !confirm(
            "⚠️ هل أنت متأكد من إرجاع هذه الفاتورة؟\nسيتم خصم المبلغ من مبيعات اليوم.",
          )
        ) {
          return;
        }

        const sale = window.currentReturnSale;

        // إنشاء سجل الإرجاع
        const returnRecord = {
          id: Date.now().toString(),
          invoiceNumber: sale.invoiceNumber,
          originalSaleId: sale.id,
          amount: sale.finalTotal,
          originalTotal: sale.total,
          discount: sale.discount || 0,
          date: new Date().toISOString(),
          reason: reason,
          returnedBy: currentUser.name,
          items: sale.items,
          orderType: sale.orderType,
          paymentMethod: sale.paymentMethod,
          originalCashier: sale.cashier,
          status: "completed",
        };

        try {
          // إضافة للإرجاعات
          returns.push(returnRecord);
          await saveReturns();

          // تحديث المبيعات (إزالة الفاتورة من المبيعات)
          const saleIndex = sales.findIndex((s) => s.id === sale.id);
          if (saleIndex !== -1) {
            sales.splice(saleIndex, 1);
            await DataManager.saveSales(sales);
          }

          // تحديث إحصائيات اليوم (خصم المبلغ)
          updateTodayStatsAfterReturn(sale.finalTotal);

          showNotification(
            `✅ تم إرجاع الفاتورة رقم ${String(sale.invoiceNumber).padStart(4, "0")} بنجاح`,
            "success",
          );

          // إغلاق النافذة
          document.querySelector(".quantity-modal-overlay").remove();
          window.currentReturnSale = null;

          // تحديث واجهة المبيعات إذا كانت مفتوحة
          if (
            document.getElementById("salesTab")?.classList.contains("active")
          ) {
            loadAdminSales();
          }
        } catch (error) {
          console.error("❌ خطأ في إرجاع الفاتورة:", error);
          showNotification("❌ حدث خطأ في إرجاع الفاتورة", "error");
        }
      }

      // عرض تقرير المرتجعات (بحجم مناسب)
      async function loadReturnsReport() {
        if (currentUser?.role !== "admin") return;

        await loadReturns();

        const modal = document.createElement("div");
        modal.className = "quantity-modal-overlay";
        modal.style.display = "flex";

        const totalReturns = returns.reduce((sum, r) => sum + r.amount, 0);
        const today = new Date().toISOString().split("T")[0];
        const todayReturns = returns.filter(
          (r) => r.date.split("T")[0] === today,
        );
        const todayTotal = todayReturns.reduce((sum, r) => sum + r.amount, 0);

        modal.innerHTML = `
        <div class="quantity-modal" style="max-width: 900px; width: 95%; max-height: 80vh; overflow-y: auto;">
            <div class="quantity-modal-header" style="padding: 12px;">
                <button class="quantity-modal-close" onclick="this.closest('.quantity-modal-overlay').remove()">
                    <i class="fas fa-times"></i>
                </button>
                <div class="quantity-modal-product" style="font-size: 16px;">
                    <i class="fas fa-undo-alt"></i>
                    تقرير المرتجعات
                </div>
            </div>
            <div class="quantity-display" style="padding: 15px;">
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 10px; margin-bottom: 15px;">
                    <div style="background: #f0f8ff; padding: 10px; border-radius: 6px; text-align: center;">
                        <div style="font-size: 12px; color: #666;">إجمالي المرتجعات</div>
                        <div style="font-size: 18px; font-weight: bold; color: var(--secondary-color);">${totalReturns.toFixed(2)} ج.م</div>
                    </div>
                    <div style="background: #fff3cd; padding: 10px; border-radius: 6px; text-align: center;">
                        <div style="font-size: 12px; color: #666;">مرتجعات اليوم</div>
                        <div style="font-size: 18px; font-weight: bold; color: #ff9800;">${todayTotal.toFixed(2)} ج.م</div>
                    </div>
                    <div style="background: #e8f5e9; padding: 10px; border-radius: 6px; text-align: center;">
                        <div style="font-size: 12px; color: #666;">عدد المرتجعات</div>
                        <div style="font-size: 18px; font-weight: bold; color: #4caf50;">${returns.length}</div>
                    </div>
                </div>
                
                <div style="overflow-x: auto;">
                    <table class="products-table" style="font-size: 13px;">
                        <thead>
                            <tr>
                                <th>رقم الفاتورة</th>
                                <th>التاريخ</th>
                                <th>المبلغ</th>
                                <th>السبب</th>
                                <th>بواسطة</th>
                            </tr>
                        </thead>
                        <tbody>
                            ${
                              returns.length === 0
                                ? '<tr><td colspan="5" style="text-align: center;">لا توجد مرتجعات</td></tr>'
                                : returns
                                    .sort(
                                      (a, b) =>
                                        new Date(b.date) - new Date(a.date),
                                    )
                                    .map(
                                      (r) => `
                                    <tr>
                                        <td style="font-weight: bold;">${String(r.invoiceNumber).padStart(4, "0")}</td>
                                        <td>${new Date(r.date).toLocaleDateString("ar-EG")}</td>
                                        <td style="color: #f44336; font-weight: bold;">${r.amount.toFixed(2)} ج.م</td>
                                        <td style="max-width: 150px; font-size: 12px;">${r.reason}</td>
                                        <td>${r.returnedBy}</td>
                                    </tr>
                                `,
                                    )
                                    .join("")
                            }
                        </tbody>
                    </table>
                </div>
                
                <div style="display: flex; gap: 8px; margin-top: 15px; justify-content: flex-end;">
                    <button class="btn btn-print" onclick="printReturnsReport()" style="padding: 8px 15px; font-size: 13px;">
                        <i class="fas fa-print"></i> طباعة
                    </button>
                    <button class="export-btn" onclick="exportReturnsToExcel()" style="padding: 8px 15px; font-size: 13px;">
                        <i class="fas fa-file-excel"></i> Excel
                    </button>
                </div>
            </div>
        </div>
    `;
        document.body.appendChild(modal);
      }

      // طباعة تقرير المرتجعات
      function printReturnsReport() {
        const printWindow = window.open("", "", "width=800,height=600");
        const totalReturns = returns.reduce((sum, r) => sum + r.amount, 0);

        const html = `
        <!DOCTYPE html>
        <html dir="rtl">
        <head>
            <meta charset="UTF-8">
            <style>
                body { font-family: Arial; padding: 20px; }
                h2, h3 { text-align: center; }
                .report-logo { width: 80px; height: 80px; border-radius: 50%; margin: 0 auto 10px; object-fit: cover; }
                table { width: 100%; border-collapse: collapse; margin: 10px 0; }
                th, td { border: 1px solid #000; padding: 8px; text-align: center; }
                .summary { background: #f9f9f9; padding: 15px; margin: 20px 0; border-radius: 5px; }
                .watermark { position: fixed; bottom: 10px; left: 10px; font-size: 10px; color: rgba(0,0,0,0.2); transform: rotate(-5deg); }
            </style>
        </head>
        <body>
            <div class="watermark">amaryasser408@gmail.com</div>
            <div style="text-align: center;">
                <img src="https://www.dropbox.com/scl/fi/fprczdxu04y7hi4ysqdqk/unnamed__4_-removebg-preview-1.png?rlkey=3f9ysoqw95oeeoc77i6jbs8h1&st=z82tk790&dl=1" class="report-logo">
                <h2>🍖 ${restaurantInfo.name}</h2>
                <h3>رقم الفرع: ${restaurantInfo.number} - ${restaurantInfo.branchName}</h3>
            </div>
            <h3>تقرير المرتجعات</h3>
            <h4>تاريخ التقرير: ${new Date().toLocaleDateString("ar-EG")}</h4>
            
            <div class="summary">
                <p><strong>إجمالي المرتجعات:</strong> ${totalReturns.toFixed(2)} جنيه</p>
                <p><strong>عدد المرتجعات:</strong> ${returns.length}</p>
            </div>
            
            <table>
                <thead>
                    <tr>
                        <th>رقم الفاتورة</th>
                        <th>التاريخ</th>
                        <th>المبلغ</th>
                        <th>السبب</th>
                        <th>بواسطة</th>
                        <th>الكاشير الأصلي</th>
                    </tr>
                </thead>
                <tbody>
                    ${returns
                      .sort((a, b) => new Date(b.date) - new Date(a.date))
                      .map(
                        (r) => `
                        <tr>
                            <td>${String(r.invoiceNumber).padStart(4, "0")}</td>
                            <td>${new Date(r.date).toLocaleDateString("ar-EG")}</td>
                            <td>${r.amount.toFixed(2)} ج.م</td>
                            <td>${r.reason}</td>
                            <td>${r.returnedBy}</td>
                            <td>${r.originalCashier || "-"}</td>
                        </tr>
                    `,
                      )
                      .join("")}
                </tbody>
            </table>
            
            <div style="margin-top: 50px; display: flex; justify-content: space-between;">
                <div style="text-align: center; width: 45%; border-top: 1px solid #000; padding-top: 10px;">
                    <p>المدير</p>
                    <p>${currentUser.name}</p>
                </div>
                <div style="text-align: center; width: 45%; border-top: 1px solid #000; padding-top: 10px;">
                    <p>ختم المطعم</p>
                </div>
            </div>
        </body>
        </html>
    `;

        printWindow.document.write(html);
        printWindow.document.close();
        printWindow.print();
      }

      // تصدير المرتجعات إلى Excel
      function exportReturnsToExcel() {
        try {
          const data = [];
          data.push(["تقرير المرتجعات", "", "", "", "", ""]);
          data.push(["المطعم:", restaurantInfo.name, "", "", "", ""]);
          data.push([
            "الفرع:",
            `${restaurantInfo.number} - ${restaurantInfo.branchName}`,
            "",
            "",
            "",
            "",
          ]);
          data.push([
            "التاريخ:",
            new Date().toLocaleDateString("ar-EG"),
            "",
            "",
            "",
            "",
          ]);
          data.push([]);

          data.push([
            "رقم الفاتورة",
            "التاريخ",
            "الوقت",
            "المبلغ",
            "السبب",
            "بواسطة",
            "الكاشير الأصلي",
            "طريقة الدفع",
          ]);

          returns
            .sort((a, b) => new Date(b.date) - new Date(a.date))
            .forEach((r) => {
              data.push([
                String(r.invoiceNumber).padStart(4, "0"),
                new Date(r.date).toLocaleDateString("ar-EG"),
                new Date(r.date).toLocaleTimeString("ar-EG"),
                r.amount,
                r.reason,
                r.returnedBy,
                r.originalCashier || "-",
                getPaymentMethodName(r.paymentMethod),
              ]);
            });

          data.push([]);
          data.push([
            "إجمالي المرتجعات:",
            returns.reduce((sum, r) => sum + r.amount, 0),
            "",
            "",
            "",
            "",
          ]);

          const ws = XLSX.utils.aoa_to_sheet(data);
          const wb = XLSX.utils.book_new();
          XLSX.utils.book_append_sheet(wb, ws, "المرتجعات");

          const today = new Date().toISOString().split("T")[0];
          XLSX.writeFile(wb, `تقرير_المرتجعات_${today}.xlsx`);

          showNotification("✅ تم تصدير تقرير المرتجعات بنجاح", "success");
        } catch (error) {
          console.error("❌ خطأ في تصدير المرتجعات:", error);
          showNotification("❌ حدث خطأ في تصدير التقرير", "error");
        }
      }

      // ==================== دوال تقارير الكاشير (مكتملة) ====================

      function getOrderTypeName(type) {
        if (!type) return "غير محدد";
        const types = {
          hall: "صالة",
          takeout: "تيك أوت",
          delivery: "توصيل",
        };
        return types[type] || type;
      }

      function getPaymentMethodName(method) {
        if (!method) return "غير محدد";
        const methods = {
          cash: "كاش",
          bank: "بنكك",
          foori: "فوري",
          okash: "أوكاش",
          sahel: "ساهل",
        };
        return methods[method] || method;
      }

      function updateCashierReportUI(filteredSales, filteredExpenses) {
        console.log("🔄 تحديث واجهة التقرير...");

        // التحقق من وجود العناصر
        const totalEl = document.getElementById("cashierReportTotal");
        const countEl = document.getElementById("cashierReportCount");
        const avgEl = document.getElementById("cashierReportAverage");
        const expEl = document.getElementById("cashierReportExpenses");
        const netEl = document.getElementById("cashierReportNet");
        const tbody = document.getElementById("cashierReportTableBody");
        const topProductsBody = document.getElementById(
          "cashierTopProductsBody",
        );

        if (!tbody) {
          console.error("❌ عنصر cashierReportTableBody غير موجود!");
          return;
        }

        // حساب الإحصائيات
        const totalSales = filteredSales.reduce(
          (sum, s) => sum + (s.finalTotal || s.total || 0),
          0,
        );
        const totalExpenses = filteredExpenses.reduce(
          (sum, e) => sum + (e.amount || 0),
          0,
        );
        const netIncome = totalSales - totalExpenses;
        const averageInvoice =
          filteredSales.length > 0 ? totalSales / filteredSales.length : 0;

        // تحديث الإحصائيات
        if (totalEl) totalEl.textContent = totalSales.toFixed(2) + " جنيه";
        if (countEl) countEl.textContent = filteredSales.length;
        if (avgEl) avgEl.textContent = averageInvoice.toFixed(2) + " جنيه";
        if (expEl) expEl.textContent = totalExpenses.toFixed(2) + " جنيه";
        if (netEl) netEl.textContent = netIncome.toFixed(2) + " جنيه";

        // تحديث جدول الفواتير
        if (filteredSales.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="9" style="text-align: center; padding: 20px;">لا توجد مبيعات في هذه الفترة</td></tr>';
        } else {
          tbody.innerHTML = filteredSales
            .map((sale) => {
              const invoiceNumber = sale.invoiceNumber
                ? String(sale.invoiceNumber).padStart(4, "0")
                : "----";
              const date = sale.date
                ? new Date(sale.date).toLocaleDateString("en-GB")
                : "----";
              const time = sale.date
                ? new Date(sale.date).toLocaleTimeString("en-US", {
                    hour: "2-digit",
                    minute: "2-digit",
                  })
                : "----";
              const orderTypeName = getOrderTypeName(sale.orderType);
              const paymentName = getPaymentMethodName(sale.paymentMethod);
              const itemsCount = sale.items ? sale.items.length : 0;
              const finalTotal = (sale.finalTotal || sale.total || 0).toFixed(
                2,
              );

              return `
                <tr>
                    <td style="font-weight: bold;">${invoiceNumber}</td>
                    <td>${date}</td>
                    <td>${time}</td>
                    <td>${orderTypeName}</td>
                    <td>${paymentName}</td>
                    <td>${itemsCount}</td>
                    <td style="color: var(--secondary-color); font-weight: bold;">${finalTotal} جنيه</td>
                    <td>
                        <button class="btn btn-info" onclick="showInvoiceModal('${sale.id}')" style="padding: 5px 10px; font-size: 12px; background: #2196F3; color: white; border: none; border-radius: 5px; cursor: pointer; margin-left: 5px;">
                            <i class="fas fa-eye"></i>
                        </button>
                        <button class="btn btn-print" onclick="printSingleInvoice('${sale.id}')" style="padding: 5px 10px; font-size: 12px; background: #607D8B; color: white; border: none; border-radius: 5px; cursor: pointer;">
                            <i class="fas fa-print"></i>
                        </button>
                    </td>
                </tr>
            `;
            })
            .join("");
        }

        // تحديث المنتجات الأكثر مبيعاً
        if (topProductsBody) {
          updateCashierTopProducts(filteredSales);
        }

        console.log("✅ تم تحديث واجهة التقرير بنجاح");
      }

      function updateCashierTopProducts(filteredSales) {
        console.log("🔄 تحديث المنتجات الأكثر مبيعاً...");

        const tbody = document.getElementById("cashierTopProductsBody");
        if (!tbody) {
          console.error("❌ عنصر cashierTopProductsBody غير موجود");
          return;
        }

        if (filteredSales.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="5" style="text-align: center; padding: 20px;">لا توجد بيانات</td></tr>';
          return;
        }

        const productStats = {};

        filteredSales.forEach((sale) => {
          if (!sale.items || !Array.isArray(sale.items)) return;

          sale.items.forEach((item) => {
            if (!item || !item.id) return;

            if (!productStats[item.id]) {
              const product = products.find((p) => p.id === item.id);
              productStats[item.id] = {
                name: product ? product.name : item.name || "منتج غير معروف",
                salesCount: 0,
                totalQuantity: 0,
                totalRevenue: 0,
              };
            }

            if (productStats[item.id]) {
              productStats[item.id].salesCount++;
              productStats[item.id].totalQuantity += item.quantity || 1;
              productStats[item.id].totalRevenue +=
                (item.price || 0) * (item.quantity || 1);
            }
          });
        });

        const sortedProducts = Object.values(productStats)
          .sort((a, b) => b.totalQuantity - a.totalQuantity)
          .slice(0, 10);

        if (sortedProducts.length === 0) {
          tbody.innerHTML =
            '<tr><td colspan="5" style="text-align: center;">لا توجد منتجات مباعة</td></tr>';
          return;
        }

        tbody.innerHTML = sortedProducts
          .map(
            (product, index) => `
        <tr>
            <td style="font-weight: bold; color: ${index === 0 ? "gold" : index === 1 ? "silver" : index === 2 ? "#cd7f32" : "inherit"}">#${index + 1}</td>
            <td>${product.name}</td>
            <td>${product.salesCount}</td>
            <td>${product.totalQuantity}</td>
            <td style="color: var(--secondary-color); font-weight: bold;">${product.totalRevenue.toFixed(2)} جنيه</td>
        </tr>
    `,
          )
          .join("");

        console.log("✅ تم تحديث المنتجات الأكثر مبيعاً");
      }

      // دالة مساعدة لطباعة فاتورة واحدة
      function printSingleInvoice(saleId) {
        const sale = sales.find((s) => s.id === saleId);
        if (sale) {
          showPrintModal(sale);
        } else {
          showNotification("❌ لم يتم العثور على الفاتورة", "error");
        }
      }

      // دالة عرض الفاتورة في نافذة منبثقة
      function showInvoiceModal(saleId) {
        const sale = sales.find((s) => s.id === saleId);
        if (!sale) {
          showNotification("❌ لم يتم العثور على الفاتورة", "error");
          return;
        }

        const modal = document.createElement("div");
        modal.className = "quantity-modal-overlay";
        modal.style.display = "flex";
        modal.innerHTML = `
        <div class="quantity-modal" style="max-width: 600px; max-height: 80vh; overflow-y: auto;">
            <div class="quantity-modal-header">
                <button class="quantity-modal-close" onclick="this.closest('.quantity-modal-overlay').remove()">
                    <i class="fas fa-times"></i>
                </button>
                <div class="quantity-modal-product">فاتورة رقم ${String(sale.invoiceNumber).padStart(4, "0")}</div>
                <div class="quantity-modal-price">${new Date(sale.date).toLocaleDateString("ar-EG")} - ${new Date(sale.date).toLocaleTimeString("ar-EG")}</div>
            </div>
            <div class="quantity-display" style="padding: 20px; text-align: right;">
                ${generateInvoiceDetailsHTML(sale)}
            </div>
            <div class="quantity-keypad">
                <div class="quantity-action-buttons">
                    <button class="quantity-action-btn quantity-cancel-btn" onclick="this.closest('.quantity-modal-overlay').remove()">
                        <i class="fas fa-times"></i> إغلاق
                    </button>
                    <button class="quantity-action-btn quantity-add-btn" onclick="printSingleInvoice('${sale.id}'); this.closest('.quantity-modal-overlay').remove();">
                        <i class="fas fa-print"></i> طباعة
                    </button>
                </div>
            </div>
        </div>
    `;
        document.body.appendChild(modal);
      }

      // دالة مساعدة لإنشاء HTML التفاصيل
      function generateInvoiceDetailsHTML(sale) {
        const orderTypeNames = {
          hall: "صالة",
          takeout: "تيك أوت",
          delivery: "توصيل",
        };
        const paymentMethodNames = {
          cash: "كاش",
          bank: "بنكك",
          foori: "فوري",
          okash: "أوكاش",
          sahel: "ساهل",
        };

        let html = `
        <div style="border-bottom: 1px solid var(--primary-color); padding-bottom: 10px; margin-bottom: 10px;">
            <p><strong>📌 نوع الطلب:</strong> ${orderTypeNames[sale.orderType] || sale.orderType}</p>
            ${sale.tableNumber ? `<p><strong>🪑 طاولة:</strong> ${sale.tableNumber}</p>` : ""}
            ${sale.customerName ? `<p><strong>👤 العميل:</strong> ${sale.customerName}</p>` : ""}
            ${sale.deliveryNumber ? `<p><strong>📞 رقم التوصيل:</strong> ${sale.deliveryNumber}</p>` : ""}
            ${sale.deliveryLocation ? `<p><strong>📍 مكان التوصيل:</strong> ${sale.deliveryLocation}</p>` : ""}
            <p><strong>💰 طريقة الدفع:</strong> ${paymentMethodNames[sale.paymentMethod] || sale.paymentMethod}</p>
            <p><strong>👨‍🍳 الكاشير:</strong> ${sale.cashier || "غير محدد"}</p>
        </div>
        <h4 style="margin: 10px 0;">المنتجات:</h4>
        <table style="width: 100%; border-collapse: collapse; margin-bottom: 10px;">
            <thead>
                <tr style="background: #f5f5f5;">
                    <th style="border: 1px solid #ddd; padding: 8px;">المنتج</th>
                    <th style="border: 1px solid #ddd; padding: 8px;">الكمية</th>
                    <th style="border: 1px solid #ddd; padding: 8px;">السعر</th>
                    <th style="border: 1px solid #ddd; padding: 8px;">الإجمالي</th>
                </tr>
            </thead>
            <tbody>
    `;

        sale.items.forEach((item) => {
          html += `
            <tr>
                <td style="border: 1px solid #ddd; padding: 8px;">${item.name}</td>
                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${item.quantity}</td>
                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${(item.price || 0).toFixed(2)}</td>
                <td style="border: 1px solid #ddd; padding: 8px; text-align: center;">${((item.price || 0) * item.quantity).toFixed(2)}</td>
            </tr>
        `;
        });

        html += `
            </tbody>
        </table>
        <div style="margin-top: 10px; border-top: 2px solid var(--secondary-color); padding-top: 10px;">
            ${sale.discount > 0 ? `<p><strong>🔻 الخصم:</strong> ${sale.discount.toFixed(2)} جنيه</p>` : ""}
            <p style="font-size: 18px; color: var(--secondary-color);"><strong>💵 الإجمالي النهائي:</strong> ${(sale.finalTotal || sale.total).toFixed(2)} جنيه</p>
        </div>
        ${sale.orderNotes ? `<div style="background: #fff3cd; padding: 8px; border-radius: 5px; margin-top: 10px;"><strong>📝 ملاحظات:</strong> ${sale.orderNotes}</div>` : ""}
    `;

        return html;
      }
    </script>
  </body>
</html>
