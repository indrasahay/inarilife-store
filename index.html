<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>INARI LIFE | Premium Curated Living</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              DEFAULT: '#111827',
              light: '#374151',
              accent: '#d97706',
              bg: '#f9fafb'
            }
          }
        }
      }
    }
  </script>
</head>
<body class="bg-gray-50 text-gray-900 font-sans antialiased min-h-screen flex flex-col">

  <!-- Header / Navigation -->
  <header class="bg-white border-b border-gray-200 sticky top-0 z-40 shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      <div class="flex items-center space-x-3">
        <span class="text-2xl font-black tracking-wider text-gray-900 uppercase">INARI LIFE</span>
        <span class="text-xs bg-amber-100 text-amber-800 font-semibold px-2.5 py-1 rounded-full uppercase tracking-widest hidden sm:inline-block">Catalogue</span>
      </div>
      <div class="flex items-center space-x-4">
        <a href="admin/" target="_blank" class="text-xs sm:text-sm font-medium bg-gray-900 text-white px-4 py-2 rounded-lg hover:bg-gray-800 transition shadow-sm flex items-center space-x-2">
          <i class="fa-solid fa-sliders"></i>
          <span>CMS Admin</span>
        </a>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 text-white py-16 px-4">
    <div class="max-w-5xl mx-auto text-center">
      <h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight mb-4">Curated Living Essentials</h1>
      <p class="text-lg sm:text-xl text-gray-300 max-w-2xl mx-auto mb-8">
        Explore our thoughtfully designed collection across home organization, kitchenware, smart gadgets, and travel essentials.
      </p>
      
      <!-- Search Bar -->
      <div class="max-w-xl mx-auto relative">
        <span class="absolute inset-y-0 left-0 flex items-center pl-4 pointer-events-none text-gray-400">
          <i class="fa-solid fa-search"></i>
        </span>
        <input type="text" id="searchInput" placeholder="Search by product name, SKU, or keyword..." 
          class="w-full pl-11 pr-4 py-3 rounded-xl bg-white/10 border border-white/20 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-amber-500 focus:bg-white/20 transition">
      </div>
    </div>
  </section>

  <!-- Main Content & Filters -->
  <main class="flex-grow max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10 w-full">
    
    <!-- Category Filter Buttons -->
    <div class="flex items-center space-x-2 overflow-x-auto pb-4 mb-8 no-scrollbar" id="categoryFilters">
      <button data-category="All" class="cat-btn px-4 py-2 rounded-full text-sm font-semibold whitespace-nowrap transition bg-gray-900 text-white shadow">
        All Products (<span id="countAll">0</span>)
      </button>
    </div>

    <!-- Results Count -->
    <div class="flex justify-between items-center mb-6">
      <p class="text-sm text-gray-600 font-medium" id="resultsCount">Showing all products</p>
      <div class="text-sm text-gray-500">
        MRP & Selling Price displayed inclusive of all taxes
      </div>
    </div>

    <!-- Product Grid -->
    <div id="productGrid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      <!-- Cards injected by JavaScript -->
    </div>

    <!-- Empty State -->
    <div id="emptyState" class="hidden text-center py-20">
      <div class="text-5xl text-gray-300 mb-4"><i class="fa-solid fa-box-open"></i></div>
      <h3 class="text-lg font-semibold text-gray-800">No products found</h3>
      <p class="text-sm text-gray-500 mt-1">Try adjusting your search terms or category filters.</p>
    </div>

  </main>

  <!-- Product Detail Modal -->
  <div id="productModal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden items-center justify-center p-4 overflow-y-auto">
    <div class="bg-white rounded-2xl max-w-3xl w-full max-h-[90vh] overflow-y-auto shadow-2xl relative transform transition-all">
      <button onclick="closeModal()" class="absolute top-4 right-4 bg-gray-100 hover:bg-gray-200 text-gray-700 w-10 h-10 rounded-full flex items-center justify-center transition z-10">
        <i class="fa-solid fa-xmark text-lg"></i>
      </button>
      <div id="modalContent" class="p-6 sm:p-8">
        <!-- Dynamic modal content -->
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-white border-t border-gray-200 py-8 text-center text-sm text-gray-500">
    <div class="max-w-7xl mx-auto px-4">
      <p class="font-semibold text-gray-800">INARI LIFE</p>
      <p class="mt-1">Static GitHub Pages Catalogue & CMS Architecture • Powered by Open-Source Git CMS</p>
    </div>
  </footer>

  <!-- Application Logic -->
  <script>
    let products = [];
    let currentCategory = 'All';
    let searchQuery = '';

    async function loadProducts() {
      try {
        const response = await fetch('data/products.json');
        products = await response.json();
        initCategories();
        renderProducts();
      } catch (err) {
        console.error('Error loading products:', err);
        document.getElementById('productGrid').innerHTML = '<p class="col-span-full text-center text-red-500">Failed to load product catalogue. Please check data/products.json.</p>';
      }
    }

    function initCategories() {
      const categories = ['All', ...new Set(products.map(p => p.category))];
      const container = document.getElementById('categoryFilters');
      
      document.getElementById('countAll').innerText = products.length;
      
      let html = `<button data-category="All" class="cat-btn px-4 py-2 rounded-full text-sm font-semibold whitespace-nowrap transition bg-gray-900 text-white shadow">All Products (${products.length})</button>`;
      
      categories.filter(c => c !== 'All').forEach(cat => {
        const count = products.filter(p => p.category === cat).length;
        html += `<button data-category="${cat}" class="cat-btn px-4 py-2 rounded-full text-sm font-semibold whitespace-nowrap transition bg-white text-gray-700 border border-gray-200 hover:bg-gray-100">${cat} (${count})</button>`;
      });
      
      container.innerHTML = html;

      document.querySelectorAll('.cat-btn').forEach(btn => {
        btn.addEventListener('click', (e) => {
          document.querySelectorAll('.cat-btn').forEach(b => {
            b.classList.remove('bg-gray-900', 'text-white', 'shadow');
            b.classList.add('bg-white', 'text-gray-700', 'border', 'border-gray-200', 'hover:bg-gray-100');
          });
          e.target.classList.remove('bg-white', 'text-gray-700', 'border', 'border-gray-200', 'hover:bg-gray-100');
          e.target.classList.add('bg-gray-900', 'text-white', 'shadow');
          
          currentCategory = e.target.getAttribute('data-category');
          renderProducts();
        });
      });
    }

    function renderProducts() {
      const grid = document.getElementById('productGrid');
      const emptyState = document.getElementById('emptyState');
      const resultsCount = document.getElementById('resultsCount');

      const filtered = products.filter(p => {
        const matchesCategory = currentCategory === 'All' || p.category === currentCategory;
        const q = searchQuery.toLowerCase();
        const matchesSearch = !q || p.title.toLowerCase().includes(q) || p.sku.toLowerCase().includes(q) || p.category.toLowerCase().includes(q) || (p.short_description && p.short_description.toLowerCase().includes(q));
        return matchesCategory && matchesSearch;
      });

      resultsCount.innerText = `Showing ${filtered.length} of ${products.length} products`;

      if (filtered.length === 0) {
        grid.innerHTML = '';
        emptyState.classList.remove('hidden');
        return;
      }

      emptyState.classList.add('hidden');

      let html = '';
      filtered.forEach(p => {
        const discount = p.mrp > p.selling_price ? Math.round(((p.mrp - p.selling_price) / p.mrp) * 100) : 0;
        
        let buyButtonHtml = '';
        if (p.status === 'Active' && p.amazon_url && p.amazon_url.trim() !== '' && p.amazon_url !== 'nan') {
          buyButtonHtml = `<a href="${p.amazon_url}" target="_blank" onclick="event.stopPropagation()" class="flex-1 bg-amber-500 hover:bg-amber-600 text-white text-center py-2 px-3 rounded-lg text-sm font-semibold transition shadow-sm flex items-center justify-center space-x-1.5"><i class="fa-brands fa-amazon"></i><span>Buy Now</span></a>`;
        } else {
          buyButtonHtml = `<button disabled class="flex-1 bg-gray-100 text-gray-400 py-2 px-3 rounded-lg text-sm font-medium cursor-not-allowed">Unavailable</button>`;
        }

        html += `
          <div onclick="openModal('${p.id}')" class="bg-white rounded-xl border border-gray-200 overflow-hidden shadow-sm hover:shadow-md transition cursor-pointer flex flex-col justify-between group">
            <div>
              <div class="relative aspect-square bg-gray-100 overflow-hidden">
                <img src="${p.main_image}" alt="${p.title}" class="w-full h-full object-cover group-hover:scale-105 transition duration-300" onerror="this.src='https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=600&auto=format&fit=crop&q=80'">
                <div class="absolute top-3 left-3 flex flex-col space-y-1">
                  ${discount > 0 ? `<span class="bg-red-500 text-white text-xs font-bold px-2 py-0.5 rounded-md shadow">-${discount}%</span>` : ''}
                </div>
                <div class="absolute top-3 right-3 bg-white/90 backdrop-blur-sm text-xs font-semibold px-2 py-1 rounded text-gray-700 shadow-sm">
                  SKU: ${p.sku}
                </div>
              </div>
              <div class="p-4">
                <p class="text-xs font-semibold text-amber-600 uppercase tracking-wider mb-1">${p.category}</p>
                <h3 class="font-semibold text-gray-900 line-clamp-2 text-base mb-2 group-hover:text-amber-600 transition">${p.title}</h3>
                <p class="text-xs text-gray-500 line-clamp-2 mb-4">${p.short_description || ''}</p>
              </div>
            </div>
            <div class="p-4 pt-0">
              <div class="flex flex-col mb-4 bg-gray-50 p-2.5 rounded-lg border border-gray-100">
                <div class="flex justify-between items-baseline">
                  <span class="text-xs text-gray-500">Selling Price:</span>
                  <span class="text-lg font-extrabold text-gray-900">₹${p.selling_price.toLocaleString('en-IN')}</span>
                </div>
                <div class="flex justify-between items-baseline mt-0.5">
                  <span class="text-xs text-gray-400">MRP:</span>
                  <span class="text-xs text-gray-400 line-through">₹${p.mrp.toLocaleString('en-IN')}</span>
                </div>
              </div>
              <div class="flex space-x-2">
                <button class="flex-1 bg-gray-100 hover:bg-gray-200 text-gray-800 py-2 px-3 rounded-lg text-sm font-semibold transition">Details</button>
                ${buyButtonHtml}
              </div>
            </div>
          </div>
        `;
      });

      grid.innerHTML = html;
    }

    function openModal(id) {
      const p = products.find(item => item.id === id);
      if (!p) return;

      const discount = p.mrp > p.selling_price ? Math.round(((p.mrp - p.selling_price) / p.mrp) * 100) : 0;

      let buyButtonHtml = '';
      if (p.status === 'Active' && p.amazon_url && p.amazon_url.trim() !== '' && p.amazon_url !== 'nan') {
        buyButtonHtml = `<a href="${p.amazon_url}" target="_blank" class="w-full bg-amber-500 hover:bg-amber-600 text-white py-3 px-6 rounded-xl font-bold text-center transition shadow flex items-center justify-center space-x-2 text-lg"><i class="fa-brands fa-amazon text-xl"></i><span>Buy Now on Amazon</span></a>`;
      } else {
        buyButtonHtml = `<div class="bg-gray-50 text-gray-500 py-3 px-6 rounded-xl font-medium text-center text-sm border border-gray-200">Online purchase via Amazon is currently unavailable for this item.</div>`;
      }

      const modalContent = document.getElementById('modalContent');
      modalContent.innerHTML = `
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="space-y-4">
            <div class="aspect-square bg-gray-100 rounded-xl overflow-hidden border border-gray-200">
              <img src="${p.main_image}" alt="${p.title}" class="w-full h-full object-cover" onerror="this.src='https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=600&auto=format&fit=crop&q=80'">
            </div>
          </div>
          <div class="flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-2">
                <span class="text-xs font-bold text-amber-600 uppercase tracking-wider">${p.category} ${p.subcategory ? '• ' + p.subcategory : ''}</span>
                <span class="text-xs bg-gray-100 text-gray-700 font-semibold px-2.5 py-1 rounded">SKU: ${p.sku}</span>
              </div>
              <h2 class="text-2xl font-extrabold text-gray-900 mb-3">${p.title}</h2>
              
              <div class="space-y-2 mb-6 bg-gray-50 p-4 rounded-xl border border-gray-100">
                <div class="flex justify-between items-baseline">
                  <span class="text-sm font-medium text-gray-600">Selling Price:</span>
                  <span class="text-2xl font-black text-gray-900">₹${p.selling_price.toLocaleString('en-IN')}</span>
                </div>
                <div class="flex justify-between items-baseline pt-2 border-t border-gray-200/60">
                  <span class="text-sm font-medium text-gray-500">Maximum Retail Price (MRP):</span>
                  <span class="text-base text-gray-500 line-through">₹${p.mrp.toLocaleString('en-IN')}</span>
                </div>
                ${discount > 0 ? `<div class="text-right text-xs text-red-600 font-bold pt-1">You Save: ${discount}% OFF</div>` : ''}
              </div>

              <p class="text-sm text-gray-600 mb-6 leading-relaxed">${p.short_description || p.full_description || ''}</p>

              ${p.features ? `
                <div class="mb-6">
                  <h4 class="text-xs font-bold uppercase text-gray-400 tracking-wider mb-2">Key Features</h4>
                  <div class="text-sm text-gray-700 space-y-1 bg-gray-50 p-3 rounded-xl border border-gray-100 whitespace-pre-line">${p.features}</div>
                </div>
              ` : ''}
            </div>

            <div class="mt-6">
              ${buyButtonHtml}
            </div>
          </div>
        </div>

        <div class="mt-8 pt-6 border-t border-gray-200 grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <h4 class="text-sm font-bold text-gray-900 mb-2">Full Description</h4>
            <p class="text-sm text-gray-600 leading-relaxed">${p.full_description || 'No detailed description provided.'}</p>
          </div>
          <div>
            <h4 class="text-sm font-bold text-gray-900 mb-2">Specifications</h4>
            <div class="text-sm text-gray-600 whitespace-pre-line bg-gray-50 p-4 rounded-xl border border-gray-100">${p.specifications || 'Standard INARI LIFE specifications apply.'}</div>
          </div>
        </div>
      `;

      const modal = document.getElementById('productModal');
      modal.classList.remove('hidden');
      modal.classList.add('flex');
    }

    function closeModal() {
      const modal = document.getElementById('productModal');
      modal.classList.add('hidden');
      modal.classList.remove('flex');
    }

    document.getElementById('searchInput').addEventListener('input', (e) => {
      searchQuery = e.target.value;
      renderProducts();
    });

    window.addEventListener('click', (e) => {
      const modal = document.getElementById('productModal');
      if (e.target === modal) {
        closeModal();
      }
    });

    loadProducts();
  </script>
</body>
</html>