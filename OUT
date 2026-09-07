<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes" />
    <title>KeuanganKu - IDR & LKR</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800;14..32,900&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem;
            background: linear-gradient(135deg, #0a2a1a 0%, #1a5c3e 40%, #2d8f5e 70%, #5cb88a 100%);
            position: relative;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.05'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: 0;
        }

        body::after {
            content: '';
            position: fixed;
            top: -20%;
            right: -10%;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.05) 0%, transparent 70%);
            pointer-events: none;
            z-index: 0;
            border-radius: 50%;
        }

        .container {
            max-width: 1100px;
            width: 100%;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-radius: 2.5rem;
            padding: 1.5rem;
            border: 1px solid rgba(255, 255, 255, 0.15);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.25);
            position: relative;
            z-index: 1;
        }

        /* ===== HEADER ===== */
        .header-flex {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin-bottom: 0.5rem;
            gap: 0.5rem;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 0.6rem;
        }

        .logo-icon {
            width: 42px;
            height: 42px;
            background: linear-gradient(145deg, #1a5c3e, #0d2b1e);
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            box-shadow: 0 6px 18px rgba(26, 92, 62, 0.25);
        }

        h1 {
            font-size: 1.5rem;
            font-weight: 900;
            color: #0a2a1a;
            letter-spacing: -0.02em;
        }

        h1 span {
            color: #1a5c3e;
        }

        .badge-month {
            background: linear-gradient(135deg, #1a5c3e, #0d2b1e);
            padding: 0.4rem 1.2rem;
            border-radius: 60px;
            font-weight: 600;
            color: white;
            font-size: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
            box-shadow: 0 4px 12px rgba(26, 92, 62, 0.2);
        }

        .badge-month i {
            font-size: 0.7rem;
        }

        .sub-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin: 0.2rem 0 1.2rem 0;
            padding: 0.3rem 0.8rem;
            background: rgba(26, 92, 62, 0.04);
            border-radius: 40px;
            gap: 0.3rem;
        }

        .sub-info p {
            color: #1a4a3a;
            font-weight: 500;
            font-size: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
            padding: 0.1rem 0.4rem;
        }

        .sub-info p i {
            color: #1a5c3e;
            font-size: 0.7rem;
        }

        /* ===== TOTAL CARDS PER MATA UANG ===== */
        .total-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0.8rem;
            margin-bottom: 1.2rem;
        }

        .currency-group {
            background: white;
            border-radius: 1.5rem;
            padding: 1rem 1.2rem;
            border: 1px solid rgba(26, 92, 62, 0.06);
            box-shadow: 0 2px 12px rgba(0, 0, 0, 0.02);
        }

        .currency-group .currency-title {
            font-size: 0.7rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            color: #4d6f82;
            opacity: 0.5;
            margin-bottom: 0.4rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }

        .currency-group .currency-title .dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            display: inline-block;
            flex-shrink: 0;
        }

        .dot-idr {
            background: #1a5c3e;
        }
        .dot-lkr {
            background: #c47a2a;
        }

        .currency-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 0.4rem;
        }

        .stat-item {
            padding: 0.2rem 0.1rem;
        }

        .stat-item .stat-label {
            font-size: 0.55rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.4px;
            color: #4d6f82;
            opacity: 0.5;
        }

        .stat-item .stat-number {
            font-weight: 900;
            font-size: 1.1rem;
            letter-spacing: -0.02em;
            display: block;
            margin-top: 0.05rem;
            word-break: break-word;
        }

        .stat-number.income {
            color: #1a5c3e;
        }
        .stat-number.expense {
            color: #c44a5a;
        }
        .stat-number.balance {
            color: #1a4a7a;
        }
        .stat-number.balance.negative {
            color: #c44a5a;
        }

        .stat-number .currency-code {
            font-size: 0.5rem;
            font-weight: 600;
            opacity: 0.4;
            margin-left: 2px;
        }

        /* ===== TABLE ===== */
        .table-wrapper {
            background: rgba(255, 255, 255, 0.5);
            border-radius: 1.5rem;
            overflow: hidden;
            border: 1px solid rgba(26, 92, 62, 0.06);
            margin-bottom: 1.2rem;
            overflow-x: auto;
            -webkit-overflow-scrolling: touch;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.78rem;
            min-width: 600px;
        }

        th {
            text-align: left;
            padding: 0.6rem 0.8rem;
            background: rgba(26, 92, 62, 0.03);
            color: #1a4052;
            font-weight: 700;
            letter-spacing: 0.3px;
            border-bottom: 2px solid rgba(26, 92, 62, 0.04);
            font-size: 0.6rem;
            text-transform: uppercase;
            white-space: nowrap;
        }

        td {
            padding: 0.5rem 0.8rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.02);
            vertical-align: middle;
        }

        tr:last-child td {
            border-bottom: none;
        }

        tr:hover td {
            background: rgba(26, 92, 62, 0.02);
        }

        .badge-type {
            padding: 0.15rem 0.7rem;
            border-radius: 40px;
            font-size: 0.55rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.3px;
            display: inline-block;
            white-space: nowrap;
        }

        .badge-income {
            background: rgba(26, 92, 62, 0.10);
            color: #1a5c3e;
        }

        .badge-expense {
            background: rgba(196, 74, 90, 0.08);
            color: #b13e4b;
        }

        .badge-currency {
            padding: 0.08rem 0.5rem;
            border-radius: 30px;
            font-size: 0.5rem;
            font-weight: 700;
            background: rgba(0, 0, 0, 0.03);
            color: #4d6f82;
            white-space: nowrap;
        }

        .amount-income {
            color: #1a5c3e;
            font-weight: 800;
        }

        .amount-expense {
            color: #c44a5a;
            font-weight: 800;
        }

        .empty-state {
            text-align: center;
            padding: 2rem 0.5rem;
            color: #5b7b8e;
        }

        .empty-state i {
            font-size: 2.5rem;
            opacity: 0.10;
            margin-bottom: 0.5rem;
            display: block;
        }

        .empty-state span {
            font-weight: 400;
            font-size: 0.85rem;
        }

        .btn-delete-row {
            background: transparent;
            border: none;
            color: #c0d0dc;
            cursor: pointer;
            transition: all 0.25s ease;
            padding: 0.2rem 0.6rem;
            border-radius: 40px;
            font-size: 0.9rem;
        }

        .btn-delete-row:hover {
            color: #c44a5a;
            background: rgba(196, 74, 90, 0.06);
            transform: scale(1.1);
        }

        .date-cell {
            text-align: center;
            font-size: 0.65rem;
            color: #5f7e91;
            white-space: nowrap;
        }

        .date-cell .time {
            font-size: 0.55rem;
            opacity: 0.6;
        }

        /* ===== INPUT SECTION ===== */
        .input-section {
            background: rgba(255, 255, 255, 0.6);
            border-radius: 1.8rem;
            padding: 1rem 1.2rem;
            margin-bottom: 1.2rem;
            border: 1px solid rgba(26, 92, 62, 0.06);
            box-shadow: 0 2px 12px rgba(0, 0, 0, 0.01);
        }

        .input-grid {
            display: flex;
            flex-direction: column;
            gap: 0.6rem;
        }

        .input-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .input-row .input-group {
            flex: 1;
            min-width: 120px;
        }

        .input-group {
            display: flex;
            flex-direction: column;
            gap: 0.2rem;
        }

        .input-group label {
            font-size: 0.6rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.4px;
            color: #1a4a3a;
            opacity: 0.5;
            display: flex;
            align-items: center;
            gap: 0.3rem;
        }

        .input-group input,
        .input-group select {
            background: white;
            border: 1.5px solid rgba(26, 92, 62, 0.08);
            border-radius: 50px;
            padding: 0.6rem 1rem;
            font-size: 0.85rem;
            transition: all 0.3s ease;
            outline: none;
            color: #0b2b3f;
            font-weight: 500;
            width: 100%;
            min-height: 44px;
        }

        .input-group input:focus,
        .input-group select:focus {
            border-color: #1a5c3e;
            box-shadow: 0 0 0 3px rgba(26, 92, 62, 0.06);
        }

        .input-group input::placeholder {
            color: #a0b8c8;
            font-weight: 400;
        }

        .toggle-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            align-items: center;
        }

        .toggle-row .input-group {
            flex: 1;
            min-width: 100px;
        }

        .currency-selector {
            display: flex;
            gap: 4px;
            background: rgba(26, 92, 62, 0.06);
            border-radius: 50px;
            padding: 4px;
            border: 1px solid rgba(26, 92, 62, 0.04);
            width: 100%;
        }

        .currency-selector button {
            border: none;
            padding: 0.4rem 0.8rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.7rem;
            cursor: pointer;
            transition: all 0.3s ease;
            background: transparent;
            color: #4d6f82;
            flex: 1;
            min-height: 38px;
        }

        .currency-selector button.active-currency {
            background: linear-gradient(135deg, #1a5c3e, #0d2b1e);
            color: white;
            box-shadow: 0 4px 12px rgba(26, 92, 62, 0.15);
        }

        .currency-selector button:hover:not(.active-currency) {
            background: rgba(0, 0, 0, 0.03);
        }

        .type-toggle {
            display: flex;
            gap: 4px;
            background: rgba(26, 92, 62, 0.06);
            border-radius: 50px;
            padding: 4px;
            border: 1px solid rgba(26, 92, 62, 0.04);
            width: 100%;
        }

        .type-toggle button {
            border: none;
            padding: 0.4rem 0.8rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.7rem;
            cursor: pointer;
            transition: all 0.3s ease;
            background: transparent;
            color: #4d6f82;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.3rem;
            flex: 1;
            min-height: 38px;
        }

        .type-toggle button.active-income {
            background: linear-gradient(135deg, #1a5c3e, #0d2b1e);
            color: white;
            box-shadow: 0 4px 12px rgba(26, 92, 62, 0.15);
        }

        .type-toggle button.active-expense {
            background: linear-gradient(135deg, #c44a5a, #a83846);
            color: white;
            box-shadow: 0 4px 12px rgba(196, 74, 90, 0.15);
        }

        .type-toggle button:hover:not(.active-income):not(.active-expense) {
            background: rgba(0, 0, 0, 0.03);
        }

        .btn-primary {
            background: linear-gradient(135deg, #1a5c3e, #0d2b1e);
            border: none;
            color: white;
            font-weight: 700;
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            font-size: 0.85rem;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 4px 16px rgba(26, 92, 62, 0.15);
            width: 100%;
            min-height: 48px;
            letter-spacing: 0.2px;
        }

        .btn-primary:active {
            transform: scale(0.97);
        }

        /* ===== ACTIONS ===== */
        .actions {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 0.5rem;
        }

        .btn-outline {
            background: rgba(255, 255, 255, 0.5);
            border: 1.5px solid rgba(26, 92, 62, 0.08);
            padding: 0.5rem 0.8rem;
            border-radius: 50px;
            font-weight: 600;
            color: #1f4052;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.4rem;
            font-size: 0.7rem;
            min-height: 40px;
            text-align: center;
        }

        .btn-outline:active {
            transform: scale(0.96);
        }

        .btn-success-outline {
            border-color: rgba(26, 92, 62, 0.15);
            color: #1a5c3e;
        }

        .btn-success-outline:active {
            background: rgba(26, 92, 62, 0.04);
        }

        .btn-danger-outline {
            border-color: rgba(196, 74, 90, 0.12);
            color: #b13e4b;
        }

        .btn-danger-outline:active {
            background: rgba(196, 74, 90, 0.04);
        }

        .footer-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin-top: 0.8rem;
            color: #4d6f82;
            font-size: 0.65rem;
            padding: 0.3rem 0.2rem;
            opacity: 0.5;
            border-top: 1px solid rgba(26, 92, 62, 0.04);
            gap: 0.3rem;
        }

        .footer-info i {
            color: #1a5c3e;
            font-size: 0.6rem;
        }

        /* ===== ANIMATIONS ===== */
        @keyframes fadeSlide {
            from {
                opacity: 0;
                transform: translateY(8px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        tr {
            animation: fadeSlide 0.2s ease-out;
        }

        /* ===== TABLET ===== */
        @media (min-width: 600px) {
            .container {
                padding: 2rem;
                border-radius: 3rem;
            }

            .total-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 1rem;
            }

            .currency-stats {
                grid-template-columns: repeat(3, 1fr);
            }

            .stat-item .stat-number {
                font-size: 1.4rem;
            }

            .input-grid {
                flex-direction: column;
            }

            .input-row {
                flex-wrap: nowrap;
            }

            .input-row .input-group {
                flex: 1;
            }

            .toggle-row .input-group {
                flex: 1;
            }

            .btn-primary {
                width: auto;
                padding: 0.7rem 2rem;
                min-width: 140px;
            }

            .actions {
                display: flex;
                justify-content: flex-end;
                gap: 0.6rem;
            }

            .btn-outline {
                padding: 0.5rem 1.2rem;
                font-size: 0.75rem;
                min-height: 36px;
            }

            .currency-selector button {
                padding: 0.4rem 1.2rem;
            }

            .type-toggle button {
                padding: 0.4rem 1.2rem;
            }

            .input-row {
                flex-wrap: wrap;
            }

            table {
                font-size: 0.82rem;
                min-width: unset;
            }

            .badge-month {
                font-size: 0.8rem;
                padding: 0.4rem 1.4rem;
            }

            h1 {
                font-size: 1.8rem;
            }
        }

        @media (min-width: 900px) {
            .container {
                padding: 2.5rem;
                border-radius: 3.5rem;
            }

            .stat-item .stat-number {
                font-size: 1.6rem;
            }

            .input-grid {
                flex-direction: row;
                flex-wrap: wrap;
                align-items: flex-end;
            }

            .input-row {
                flex-wrap: nowrap;
            }

            .input-row .input-group {
                flex: 1;
            }

            .toggle-row {
                flex-wrap: nowrap;
            }

            .toggle-row .input-group {
                flex: 0 0 auto;
            }

            .currency-selector {
                width: auto;
            }

            .type-toggle {
                width: auto;
            }

            .btn-primary {
                width: auto;
            }
        }

        /* ===== MOBILE FIRST - extra small ===== */
        @media (max-width: 480px) {
            .container {
                padding: 0.8rem;
                border-radius: 1.8rem;
            }

            .logo-icon {
                width: 36px;
                height: 36px;
                font-size: 1rem;
                border-radius: 12px;
            }

            h1 {
                font-size: 1.2rem;
            }

            .badge-month {
                font-size: 0.65rem;
                padding: 0.3rem 0.8rem;
            }

            .badge-month i {
                font-size: 0.6rem;
            }

            .sub-info p {
                font-size: 0.65rem;
            }

            .stat-item .stat-number {
                font-size: 0.95rem;
            }

            .stat-item .stat-label {
                font-size: 0.5rem;
            }

            .currency-group {
                padding: 0.8rem 0.8rem;
                border-radius: 1.2rem;
            }

            .currency-group .currency-title {
                font-size: 0.6rem;
            }

            .input-section {
                padding: 0.8rem;
                border-radius: 1.4rem;
            }

            .input-group input,
            .input-group select {
                padding: 0.5rem 0.8rem;
                font-size: 0.8rem;
                min-height: 38px;
            }

            .input-group label {
                font-size: 0.55rem;
            }

            .currency-selector button {
                font-size: 0.65rem;
                padding: 0.3rem 0.5rem;
                min-height: 32px;
            }

            .type-toggle button {
                font-size: 0.65rem;
                padding: 0.3rem 0.5rem;
                min-height: 32px;
            }

            .btn-primary {
                font-size: 0.8rem;
                padding: 0.6rem;
                min-height: 42px;
            }

            .btn-outline {
                font-size: 0.6rem;
                padding: 0.4rem 0.5rem;
                min-height: 34px;
            }

            .actions {
                gap: 0.3rem;
            }

            table {
                font-size: 0.65rem;
                min-width: 480px;
            }

            th {
                padding: 0.4rem 0.5rem;
                font-size: 0.5rem;
            }

            td {
                padding: 0.35rem 0.5rem;
            }

            .badge-type {
                font-size: 0.5rem;
                padding: 0.1rem 0.5rem;
            }

            .badge-currency {
                font-size: 0.45rem;
                padding: 0.05rem 0.4rem;
            }

            .date-cell {
                font-size: 0.55rem;
            }

            .date-cell .time {
                font-size: 0.45rem;
            }

            .btn-delete-row {
                font-size: 0.75rem;
                padding: 0.15rem 0.4rem;
            }

            .footer-info {
                font-size: 0.55rem;
            }

            .empty-state i {
                font-size: 2rem;
            }

            .empty-state span {
                font-size: 0.75rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- ===== HEADER ===== -->
        <div class="header-flex">
            <div class="logo-area">
                <div class="logo-icon"><i class="fas fa-wallet"></i></div>
                <h1>Keuangan<span>Ku</span></h1>
            </div>
            <div class="badge-month">
                <i class="fas fa-calendar-alt"></i> <span id="currentMonth"></span>
            </div>
        </div>

        <div class="sub-info">
            <p><i class="fas fa-list-ul"></i> <span id="entryCount">0</span> transaksi</p>
            <p><i class="fas fa-clock"></i> <span id="lastSaved">Belum disimpan</span></p>
        </div>

        <!-- ===== TOTAL CARDS PER MATA UANG ===== -->
        <div class="total-grid" id="totalGrid">
            <!-- IDR Group -->
            <div class="currency-group">
                <div class="currency-title">
                    <span class="dot dot-idr"></span> IDR
                </div>
                <div class="currency-stats">
                    <div class="stat-item">
                        <div class="stat-label">Pemasukan</div>
                        <span class="stat-number income" id="totalIncomeIDR">Rp 0</span>
                    </div>
                    <div class="stat-item">
                        <div class="stat-label">Pengeluaran</div>
                        <span class="stat-number expense" id="totalExpenseIDR">Rp 0</span>
                    </div>
                    <div class="stat-item">
                        <div class="stat-label">Saldo</div>
                        <span class="stat-number balance" id="balanceIDR">Rp 0</span>
                    </div>
                </div>
            </div>

            <!-- LKR Group -->
            <div class="currency-group">
                <div class="currency-title">
                    <span class="dot dot-lkr"></span> LKR
                </div>
                <div class="currency-stats">
                    <div class="stat-item">
                        <div class="stat-label">Pemasukan</div>
                        <span class="stat-number income" id="totalIncomeLKR">Rs 0</span>
                    </div>
                    <div class="stat-item">
                        <div class="stat-label">Pengeluaran</div>
                        <span class="stat-number expense" id="totalExpenseLKR">Rs 0</span>
                    </div>
                    <div class="stat-item">
                        <div class="stat-label">Saldo</div>
                        <span class="stat-number balance" id="balanceLKR">Rs 0</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== TABLE ===== -->
        <div class="table-wrapper">
            <table>
                <thead>
                    <tr>
                        <th>Deskripsi</th>
                        <th>Kategori</th>
                        <th style="text-align:center;">Jenis</th>
                        <th style="text-align:center;">Mata Uang</th>
                        <th style="text-align:right;">Jumlah</th>
                        <th style="text-align:center;">Tanggal</th>
                        <th style="text-align:center; width:30px;"></th>
                    </tr>
                </thead>
                <tbody id="tableBody">
                    <!-- data via js -->
                </tbody>
            </table>
        </div>

        <!-- ===== INPUT FORM ===== -->
        <div class="input-section">
            <div class="input-grid">
                <div class="input-row">
                    <div class="input-group" style="flex:2;">
                        <label for="descInput"><i class="fas fa-pen"></i> Deskripsi</label>
                        <input type="text" id="descInput" placeholder="Contoh: Gaji, Makan siang" />
                    </div>
                    <div class="input-group" style="flex:1;">
                        <label for="amountInput"><i class="fas fa-rupiah-sign"></i> Jumlah</label>
                        <input type="text" id="amountInput" placeholder="0" inputmode="numeric" />
                    </div>
                </div>
                <div class="input-row">
                    <div class="input-group" style="flex:1.5;">
                        <label for="categorySelect"><i class="fas fa-tags"></i> Kategori</label>
                        <select id="categorySelect">
                            <option value="Pemasukan">💰 Pemasukan</option>
                            <option value="Makanan">🍽️ Makanan</option>
                            <option value="Transportasi">🚗 Transportasi</option>
                            <option value="Belanja">🛍️ Belanja</option>
                            <option value="Tagihan">🧾 Tagihan</option>
                            <option value="Hiburan">🎬 Hiburan</option>
                            <option value="Kesehatan">💊 Kesehatan</option>
                            <option value="Pendidikan">📚 Pendidikan</option>
                            <option value="Lainnya">📌 Lainnya</option>
                        </select>
                    </div>
                </div>
                <div class="toggle-row">
                    <div class="input-group" style="flex:1;">
                        <label>Mata Uang</label>
                        <div class="currency-selector" id="currencySelector">
                            <button class="active-currency" data-currency="IDR" id="idrBtn">IDR</button>
                            <button data-currency="LKR" id="lkrBtn">LKR</button>
                        </div>
                    </div>
                    <div class="input-group" style="flex:1;">
                        <label>Jenis</label>
                        <div class="type-toggle" id="typeToggle">
                            <button class="active-income" data-type="income" id="incomeToggle"><i class="fas fa-arrow-up"></i> Masuk</button>
                            <button data-type="expense" id="expenseToggle"><i class="fas fa-arrow-down"></i> Keluar</button>
                        </div>
                    </div>
                </div>
                <button class="btn-primary" id="addBtn"><i class="fas fa-plus-circle"></i> Tambah Transaksi</button>
            </div>
        </div>

        <!-- ===== ACTIONS ===== -->
        <div class="actions">
            <button class="btn-outline btn-danger-outline" id="clearBtn"><i class="fas fa-trash-can"></i> Hapus</button>
            <button class="btn-outline btn-success-outline" id="saveBtn"><i class="fas fa-floppy-disk"></i> Simpan</button>
            <button class="btn-outline" id="exportBtn"><i class="fas fa-file-arrow-down"></i> CSV</button>
        </div>

        <div class="footer-info">
            <span><i class="fas fa-database"></i> Data tersimpan otomatis</span>
            <span><i class="fas fa-rotate"></i> <span id="lastSavedTime">-</span></span>
        </div>
    </div>

    <script>
        (function() {
            // ========== STATE ==========
            let transactions = [];
            let nextId = 1;
            let selectedType = 'income';
            let selectedCurrency = 'IDR';

            // DOM refs
            const tbody = document.getElementById('tableBody');
            const totalIncomeIDREl = document.getElementById('totalIncomeIDR');
            const totalExpenseIDREl = document.getElementById('totalExpenseIDR');
            const balanceIDREl = document.getElementById('balanceIDR');
            const totalIncomeLKREl = document.getElementById('totalIncomeLKR');
            const totalExpenseLKREl = document.getElementById('totalExpenseLKR');
            const balanceLKREl = document.getElementById('balanceLKR');
            const entryCount = document.getElementById('entryCount');
            const currentMonthSpan = document.getElementById('currentMonth');
            const lastSavedSpan = document.getElementById('lastSaved');
            const lastSavedTime = document.getElementById('lastSavedTime');

            const descInput = document.getElementById('descInput');
            const amountInput = document.getElementById('amountInput');
            const categorySelect = document.getElementById('categorySelect');
            const addBtn = document.getElementById('addBtn');
            const clearBtn = document.getElementById('clearBtn');
            const saveBtn = document.getElementById('saveBtn');
            const exportBtn = document.getElementById('exportBtn');
            const incomeToggle = document.getElementById('incomeToggle');
            const expenseToggle = document.getElementById('expenseToggle');
            const idrBtn = document.getElementById('idrBtn');
            const lkrBtn = document.getElementById('lkrBtn');

            // ========== HELPERS ==========
            function formatCurrency(amount, currency) {
                const symbol = currency === 'IDR' ? 'Rp' : 'Rs';
                return symbol + ' ' + Number(amount).toLocaleString('id-ID');
            }

            function formatNumberInput(value) {
                let num = value.replace(/[^0-9]/g, '');
                if (num === '') return '';
                return Number(num).toLocaleString('id-ID');
            }

            function parseNumberInput(value) {
                return parseInt(value.replace(/[^0-9]/g, '')) || 0;
            }

            function getCurrentMonth() {
                const d = new Date();
                return d.toLocaleString('id-ID', { month: 'long', year: 'numeric' });
            }

            function formatDate(dateString) {
                const d = new Date(dateString);
                return d.toLocaleDateString('id-ID', { day: '2-digit', month: 'short', year: 'numeric' });
            }

            function formatTime(dateString) {
                const d = new Date(dateString);
                return d.toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit' });
            }

            function escapeHtml(text) {
                const div = document.createElement('div');
                div.textContent = text;
                return div.innerHTML;
            }

            function updateLastSavedTime() {
                const now = new Date();
                const timeStr = now.toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit',
                    second: '2-digit' });
                lastSavedTime.textContent = timeStr;
                lastSavedSpan.textContent = 'Tersimpan ' + timeStr;
            }

            // ========== RENDER ==========
            function render() {
                if (transactions.length === 0) {
                    tbody.innerHTML = `
                    <tr><td colspan="7" class="empty-state">
                      <i class="fas fa-receipt"></i>
                      <span>Belum ada transaksi</span>
                    </td></tr>
                  `;
                    totalIncomeIDREl.textContent = 'Rp 0';
                    totalExpenseIDREl.textContent = 'Rp 0';
                    balanceIDREl.textContent = 'Rp 0';
                    totalIncomeLKREl.textContent = 'Rs 0';
                    totalExpenseLKREl.textContent = 'Rs 0';
                    balanceLKREl.textContent = 'Rs 0';
                    entryCount.textContent = '0';
                    return;
                }

                const sorted = [...transactions].sort((a, b) => b.id - a.id);
                let html = '';
                let totalIncomeIDR = 0,
                    totalExpenseIDR = 0;
                let totalIncomeLKR = 0,
                    totalExpenseLKR = 0;

                sorted.forEach(t => {
                    if (t.type === 'income') {
                        if (t.currency === 'IDR') totalIncomeIDR += t.amount;
                        else totalIncomeLKR += t.amount;
                    } else {
                        if (t.currency === 'IDR') totalExpenseIDR += t.amount;
                        else totalExpenseLKR += t.amount;
                    }

                    const typeLabel = t.type === 'income' ? 'Pemasukan' : 'Pengeluaran';
                    const badgeClass = t.type === 'income' ? 'badge-income' : 'badge-expense';
                    const amountClass = t.type === 'income' ? 'amount-income' : 'amount-expense';
                    const sign = t.type === 'income' ? '+' : '−';
                    const currencyLabel = t.currency === 'IDR' ? 'IDR' : 'LKR';

                    html += `
                    <tr>
                      <td><strong>${escapeHtml(t.desc)}</strong></td>
                      <td><span class="badge-type ${badgeClass}">${escapeHtml(t.category)}</span></td>
                      <td style="text-align:center;"><span class="badge-type ${badgeClass}">${typeLabel}</span></td>
                      <td style="text-align:center;"><span class="badge-currency">${currencyLabel}</span></td>
                      <td style="text-align:right; font-weight:800;" class="${amountClass}">${sign} ${formatCurrency(t.amount, t.currency)}</td>
                      <td class="date-cell">
                        <div>${formatDate(t.date)}</div>
                        <div class="time">${formatTime(t.date)}</div>
                      </td>
                      <td style="text-align:center;">
                        <button class="btn-delete-row" data-id="${t.id}" title="Hapus">
                          <i class="fas fa-trash-can"></i>
                        </button>
                      </td>
                    </tr>
                  `;
                });
                tbody.innerHTML = html;

                // Update IDR stats
                const balanceIDR = totalIncomeIDR - totalExpenseIDR;
                totalIncomeIDREl.textContent = formatCurrency(totalIncomeIDR, 'IDR');
                totalExpenseIDREl.textContent = formatCurrency(totalExpenseIDR, 'IDR');
                balanceIDREl.textContent = formatCurrency(balanceIDR, 'IDR');
                balanceIDREl.className = 'stat-number balance' + (balanceIDR < 0 ? ' negative' : '');

                // Update LKR stats
                const balanceLKR = totalIncomeLKR - totalExpenseLKR;
                totalIncomeLKREl.textContent = formatCurrency(totalIncomeLKR, 'LKR');
                totalExpenseLKREl.textContent = formatCurrency(totalExpenseLKR, 'LKR');
                balanceLKREl.textContent = formatCurrency(balanceLKR, 'LKR');
                balanceLKREl.className = 'stat-number balance' + (balanceLKR < 0 ? ' negative' : '');

                entryCount.textContent = transactions.length;
            }

            // ========== CRUD ==========
            function addTransaction(desc, amount, category, type, currency) {
                if (!desc.trim()) {
                    alert('⚠️ Deskripsi tidak boleh kosong.');
                    return false;
                }
                if (isNaN(amount) || amount < 500) {
                    alert('⚠️ Jumlah minimal 500.');
                    return false;
                }
                const newT = {
                    id: nextId++,
                    desc: desc.trim(),
                    amount: Number(amount),
                    category: category || (type === 'income' ? 'Pemasukan' : 'Lainnya'),
                    type: type,
                    currency: currency || 'IDR',
                    date: new Date().toISOString()
                };
                transactions.push(newT);
                render();
                updateStorage();
                return true;
            }

            function deleteTransaction(id) {
                if (confirm('Hapus transaksi ini?')) {
                    transactions = transactions.filter(t => t.id !== id);
                    render();
                    updateStorage();
                }
            }

            function clearAll() {
                if (transactions.length === 0) {
                    alert('Tidak ada data untuk dihapus.');
                    return;
                }
                if (confirm('Hapus SEMUA data keuangan?')) {
                    transactions = [];
                    nextId = 1;
                    render();
                    updateStorage();
                }
            }

            // ========== STORAGE ==========
            function updateStorage() {
                try {
                    const data = { transactions, nextId };
                    localStorage.setItem('financeData', JSON.stringify(data));
                    updateLastSavedTime();
                } catch (e) { console.warn('Gagal simpan', e); }
            }

            function loadStorage() {
                try {
                    const stored = localStorage.getItem('financeData');
                    if (stored) {
                        const parsed = JSON.parse(stored);
                        if (parsed.transactions && Array.isArray(parsed.transactions)) {
                            transactions = parsed.transactions;
                            nextId = parsed.nextId || (transactions.length ? Math.max(...transactions.map(t => t
                                .id)) + 1 : 1);
                            render();
                            updateLastSavedTime();
                            lastSavedSpan.textContent = 'Dimuat dari penyimpanan';
                            return true;
                        }
                    }
                } catch (e) {}
                return false;
            }

            // ========== EXPORT CSV ==========
            function exportCSV() {
                if (transactions.length === 0) {
                    alert('Tidak ada data untuk diekspor.');
                    return;
                }
                const header = 'Deskripsi,Kategori,Jenis,Mata Uang,Jumlah,Tanggal,Waktu\n';
                const rows = transactions.map(t => {
                    const date = new Date(t.date);
                    const dateStr = date.toLocaleDateString('id-ID');
                    const timeStr = date.toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit' });
                    const typeLabel = t.type === 'income' ? 'Pemasukan' : 'Pengeluaran';
                    return `"${t.desc}","${t.category}","${typeLabel}","${t.currency}",${t.amount},"${dateStr}","${timeStr}"`;
                }).join('\n');
                const csv = header + rows;
                const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
                const link = document.createElement('a');
                link.href = URL.createObjectURL(blob);
                link.download = `keuangan_${new Date().toISOString().slice(0,10)}.csv`;
                link.click();
                URL.revokeObjectURL(link.href);
            }

            // ========== TOGGLES ==========
            function setType(type) {
                selectedType = type;
                incomeToggle.className = '';
                expenseToggle.className = '';
                if (type === 'income') {
                    incomeToggle.classList.add('active-income');
                } else {
                    expenseToggle.classList.add('active-expense');
                }
            }

            function setCurrency(currency) {
                selectedCurrency = currency;
                idrBtn.className = '';
                lkrBtn.className = '';
                if (currency === 'IDR') {
                    idrBtn.classList.add('active-currency');
                } else {
                    lkrBtn.classList.add('active-currency');
                }
            }

            // ========== INPUT FORMATING ==========
            amountInput.addEventListener('input', function() {
                const cursorPos = this.selectionStart;
                const raw = this.value;
                const formatted = formatNumberInput(raw);
                this.value = formatted;
                const newPos = cursorPos + (formatted.length - raw.length);
                this.setSelectionRange(Math.min(newPos, this.value.length), Math.min(newPos, this.value.length));
            });

            amountInput.addEventListener('focus', function() {
                const raw = this.value;
                if (raw) {
                    const numeric = parseNumberInput(raw);
                    this.value = numeric.toString();
                }
            });

            amountInput.addEventListener('blur', function() {
                const raw = this.value;
                if (raw) {
                    const numeric = parseNumberInput(raw);
                    if (numeric > 0) {
                        this.value = formatNumberInput(numeric.toString());
                    } else {
                        this.value = '';
                    }
                }
            });

            // ========== INIT ==========
            function init() {
                currentMonthSpan.textContent = getCurrentMonth();

                const loaded = loadStorage();
                if (!loaded) {
                    transactions = [
                        { id: 1, desc: 'GAJI BULANAN', amount: 5000000, category: 'Pemasukan', type: 'income',
                            currency: 'IDR', date: new Date().toISOString() },
                        { id: 2, desc: 'MAKAN SIANG', amount: 35000, category: 'Makanan', type: 'expense',
                            currency: 'IDR', date: new Date(Date.now() - 86400000).toISOString() },
                        { id: 3, desc: 'FREELANCE', amount: 25000, category: 'Pemasukan', type: 'income',
                            currency: 'LKR', date: new Date(Date.now() - 172800000).toISOString() },
                        { id: 4, desc: 'TRANSPORT', amount: 15000, category: 'Transportasi', type: 'expense',
                            currency: 'LKR', date: new Date(Date.now() - 259200000).toISOString() }
                    ];
                    nextId = 5;
                    render();
                    updateStorage();
                }

                // Type toggle
                incomeToggle.addEventListener('click', function(e) {
                    e.preventDefault();
                    setType('income');
                });
                expenseToggle.addEventListener('click', function(e) {
                    e.preventDefault();
                    setType('expense');
                });
                setType('income');

                // Currency toggle
                idrBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    setCurrency('IDR');
                });
                lkrBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    setCurrency('LKR');
                });
                setCurrency('IDR');

                // Add
                addBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    const desc = descInput.value.trim();
                    const rawAmount = amountInput.value;
                    const amount = parseNumberInput(rawAmount);
                    const category = categorySelect.value;
                    if (addTransaction(desc, amount, category, selectedType, selectedCurrency)) {
                        descInput.value = '';
                        amountInput.value = '';
                        descInput.focus();
                    }
                });

                // Enter
                amountInput.addEventListener('keypress', function(e) {
                    if (e.key === 'Enter') { e.preventDefault();
                        addBtn.click(); }
                });
                descInput.addEventListener('keypress', function(e) {
                    if (e.key === 'Enter') { e.preventDefault();
                        amountInput.focus(); }
                });

                // Clear
                clearBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    clearAll();
                });

                // Save
                saveBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    updateStorage();
                    alert('✅ Data berhasil disimpan!');
                });

                // Export
                exportBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    exportCSV();
                });

                // Delete row (delegation)
                tbody.addEventListener('click', function(e) {
                    const target = e.target.closest('.btn-delete-row');
                    if (target) {
                        e.preventDefault();
                        const id = Number(target.dataset.id);
                        if (!isNaN(id)) deleteTransaction(id);
                    }
                });
            }

            init();
        })();
    </script>
</body>
</html>
