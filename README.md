<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Punjab Flood Relief Fund – Donate</title>
  <meta name="description" content="Donate to the Punjab Flood Relief Fund. 100% of funds go directly to partnered government NGO via UPI. Every rupee counts." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    :root { --brand:#C62828; --ink:#0f172a; --sky:#0ea5e9; }
    body { font-family: 'Inter', system-ui, -apple-system, Segoe UI, Roboto, 'Helvetica Neue', Arial, 'Noto Sans', 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji'; }
    .glass { backdrop-filter: blur(10px); background: rgba(255,255,255,0.8); }
    .btn { @apply px-4 py-3 rounded-2xl font-semibold shadow hover:shadow-lg transition active:scale-[.98]; }
    .btn-primary { background: var(--brand); color:#fff; }
    .btn-outline { @apply border; border-color:#e5e7eb; color:var(--ink); }
    .pill { @apply px-4 py-2 rounded-full text-sm font-semibold cursor-pointer border; }
    .grid-cards { grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); }
  </style>
</head>
<body class="bg-slate-50 text-slate-900">
  <!-- HERO -->
  <header class="relative overflow-hidden">
    <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1540202404-c0d1d3a2f3d4?q=80&w=1400&auto=format&fit=crop')] bg-cover bg-center opacity-30"></div>
    <div class="relative mx-auto max-w-6xl px-4 pt-10 pb-16">
      <div class="glass rounded-3xl p-6 md:p-10 shadow-xl">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-[var(--brand)] text-white grid place-items-center font-extrabold">PF</div>
          <p class="text-xs md:text-sm font-semibold tracking-wide text-[var(--brand)] uppercase">Punjab Flood Relief Fund</p>
        </div>
        <h1 class="mt-4 text-3xl md:text-5xl font-extrabold leading-tight text-slate-900">
          ₹10 can give shelter — your kindness can save lives
        </h1>
        <p class="mt-3 md:mt-4 text-slate-700 max-w-3xl">
          100% of your donation is transferred directly to our partnered government NGO for immediate relief: food, temporary shelter, and medical aid.
        </p>
        <div class="mt-6 flex flex-wrap items-center gap-3">
          <span class="pill bg-white/70">Disaster Relief</span>
          <span class="pill bg-white/70">Direct-to-NGO</span>
          <span class="pill bg-white/70">Every Rupee Counts</span>
        </div>
      </div>
    </div>
  </header>

  <!-- DONATION MODULE -->
  <main class="mx-auto max-w-6xl px-4 -mt-10 pb-24">
    <section class="grid md:grid-cols-2 gap-6">
      <!-- Left: Payment Card -->
      <div class="bg-white rounded-3xl shadow-xl p-6 md:p-8">
        <h2 class="text-2xl md:text-3xl font-extrabold">Donate securely</h2>
        <p class="mt-1 text-slate-600 text-sm md:text-base">Choose an amount or enter your own. Tap a button to open your UPI app instantly.</p>

        <!-- Preset amounts -->
        <div class="mt-6 grid grid-cols-3 gap-3">
          <button class="btn btn-outline" data-amount="10">₹10</button>
          <button class="btn btn-outline" data-amount="50">₹50</button>
          <button class="btn btn-outline" data-amount="100">₹100</button>
          <button class="btn btn-outline" data-amount="250">₹250</button>
          <button class="btn btn-outline" data-amount="500">₹500</button>
          <button class="btn btn-outline" data-amount="1000">₹1000</button>
        </div>

        <!-- Custom amount -->
        <div class="mt-5">
          <label for="amount" class="block text-sm font-semibold">Custom amount (INR)</label>
          <div class="mt-2 flex gap-3">
            <input id="amount" type="number" min="1" step="1" placeholder="Enter amount" class="w-full rounded-xl border px-4 py-3 outline-none focus:ring-2 focus:ring-[var(--sky)]" />
            <button id="payBtn" class="btn btn-primary whitespace-nowrap">Pay via UPI</button>
          </div>
          <p id="amountHelp" class="mt-2 text-xs text-slate-500">Tip: Even ₹10 can provide emergency shelter materials.</p>
        </div>

        <!-- QR + copy UPI -->
        <div class="mt-8 grid grid-cols-1 sm:grid-cols-2 gap-6 items-center">
          <div class="rounded-2xl border p-4 text-center">
            <!-- Replace qr.png with your actual QR image file (e.g., sahil-upi-qr.png). -->
            <img src="qr.png" alt="Scan to donate via UPI" class="mx-auto w-52 h-52 object-contain"/>
            <p class="mt-2 text-sm text-slate-600">Scan with any UPI app</p>
          </div>
          <div>
            <p class="text-xs uppercase tracking-wide text-slate-500 font-semibold">UPI ID</p>
            <div class="mt-2 flex items-center gap-2">
              <code id="upiId" class="bg-slate-100 rounded-lg px-3 py-2 text-sm select-all">sahilmondalmd123@oksbi</code>
              <button id="copyBtn" class="btn btn-outline">Copy</button>
            </div>
            <p class="mt-3 text-sm text-slate-600">Name: <span class="font-semibold">Sahil Mondal</span></p>
            <p class="mt-1 text-xs text-slate-500">Note: If the UPI deep link doesn’t open automatically, copy the UPI ID and pay from your app.</p>
          </div>
        </div>

        <div class="mt-6 flex flex-wrap items-center gap-3">
          <a id="upiIntent" href="#" class="btn btn-primary">Open UPI App</a>
          <button id="whatsBtn" class="btn btn-outline">Share on WhatsApp</button>
        </div>

        <p class="mt-4 text-xs text-slate-500">By donating, you agree that funds are transferred directly to our partnered government NGO for relief operations.</p>
      </div>

      <!-- Right: Impact / Credibility -->
      <aside class="bg-white rounded-3xl shadow-xl p-6 md:p-8">
        <h3 class="text-xl md:text-2xl font-extrabold">Why your help matters</h3>
        <ul class="mt-4 space-y-3 text-slate-700">
          <li class="flex gap-3"><span class="text-[var(--brand)]">◆</span> Over <span class="font-semibold">1,400+</span> villages affected; thousands displaced.</li>
          <li class="flex gap-3"><span class="text-[var(--brand)]">◆</span> Immediate needs: shelter tarpaulins, dry rations, clean water, medicines.</li>
          <li class="flex gap-3"><span class="text-[var(--brand)]">◆</span> Your donation is routed <span class="font-semibold">directly</span> to a government‑partnered NGO for rapid deployment.</li>
          <li class="flex gap-3"><span class="text-[var(--brand)]">◆</span> Transparent reporting: we publish periodic relief updates.</li>
        </ul>

        <div class="mt-6 grid grid-cards gap-4">
          <div class="rounded-2xl border p-4">
            <p class="text-sm text-slate-500">For ₹10</p>
            <p class="text-lg font-bold">Emergency shelter items</p>
          </div>
          <div class="rounded-2xl border p-4">
            <p class="text-sm text-slate-500">For ₹100</p>
            <p class="text-lg font-bold">One family dry‑ration kit</p>
          </div>
          <div class="rounded-2xl border p-4">
            <p class="text-sm text-slate-500">For ₹500</p>
            <p class="text-lg font-bold">Clean‑water & hygiene supplies</p>
          </div>
        </div>

        <blockquote class="mt-6 border-l-4 pl-4 italic text-slate-600">
          “No one has ever become poor from giving.” — Anne Frank
        </blockquote>
      </aside>
    </section>
  </main>

  <footer class="border-t py-10 text-center text-sm text-slate-500">
    © <span id="yr"></span> Punjab Flood Relief Fund • Every rupee counts
  </footer>

  <script>
    // ------- CONFIG: Set your UPI details here -------
    const UPI_ID = 'sahilmondalmd123@oksbi'; // <-- your UPI ID
    const UPI_NAME = 'Sahil Mondal';         // <-- your display name
    const UPI_NOTE = 'Punjab Flood Relief';  // transaction note
    const CURRENCY = 'INR';

    // Set footer year
    document.getElementById('yr').textContent = new Date().getFullYear();

    // Build a UPI deep link for the given amount
    function buildUpiLink(amount) {
      const params = new URLSearchParams({
        pa: UPI_ID,   // payee address
        pn: UPI_NAME, // payee name
        am: amount?.toString() || '',
        cu: CURRENCY,
        tn: UPI_NOTE,
      });
      return `upi://pay?${params.toString()}`;
    }

    // Handle preset amount buttons
    document.querySelectorAll('[data-amount]').forEach(btn => {
      btn.addEventListener('click', () => {
        const amt = btn.getAttribute('data-amount');
        document.getElementById('amount').value = amt;
        document.getElementById('upiIntent').setAttribute('href', buildUpiLink(amt));
      });
    });

    // Handle custom Pay via UPI button
    document.getElementById('payBtn').addEventListener('click', () => {
      const amt = parseInt(document.getElementById('amount').value, 10);
      if (!amt || amt < 1) {
        alert('Please enter a valid amount (₹1 or more).');
        return;
      }
      window.location.href = buildUpiLink(amt);
    });

    // Primary UPI intent link (updates when typing)
    const amountInput = document.getElementById('amount');
    const upiLink = document.getElementById('upiIntent');
    amountInput.addEventListener('input', () => {
      const v = parseInt(amountInput.value || '0', 10);
      upiLink.setAttribute('href', buildUpiLink(v > 0 ? v : ''));
    });

    // Copy UPI ID
    document.getElementById('copyBtn').addEventListener('click', async () => {
      try {
        await navigator.clipboard.writeText(UPI_ID);
        const old = document.getElementById('copyBtn').textContent;
        document.getElementById('copyBtn').textContent = 'Copied!';
        setTimeout(()=>{ document.getElementById('copyBtn').textContent = old; }, 1500);
      } catch (e) {
        alert('Copy failed. Select the UPI ID and copy manually.');
      }
    });

    // WhatsApp share
    document.getElementById('whatsBtn').addEventListener('click', () => {
      const amt = document.getElementById('amount').value || '10';
      const msg = `🌊 Punjab Flood Relief Fund\n🙏 Even ₹10 can give shelter.\nTap to donate via UPI now → ${buildUpiLink(amt)}\nUPI ID: ${UPI_ID}`;
      const url = `https://wa.me/?text=${encodeURIComponent(msg)}`;
      window.open(url, '_blank');
    });

    // Initialize default link
    upiLink.setAttribute('href', buildUpiLink(''));
  </script>
</body>
</html>
