<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>IceLux — Premium Ice Cream</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Bootstrap Icons -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">

    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&display=swap" rel="stylesheet">

    <meta name="description" content="IceLux — handcrafted premium ice cream made with the finest ingredients." />

    <style>
      :root{
        --accent: #f6c1c7;
        --accent-dark: #f299a6;
        --cream: #fff8f2;
        --choco: #3b2f2f;
        --muted: #6c6c72;
        --glass: rgba(255,255,255,0.12);
      }

      html,body{height:100%;}
      body{
        font-family: 'Montserrat', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
        color: var(--choco);
        background: linear-gradient(180deg,#fff 0%, #fff8f8 100%);
      }

      /* NAVBAR */
      .navbar-brand{font-weight:800; letter-spacing:1px; color:var(--choco) !important;}
      .nav-link{color:rgba(59,47,47,0.9) !important;}
      .nav-link.active{font-weight:600; color:var(--choco) !important}

      /* HERO */
      .hero{
        background-image: url('images/hero.jpg');
        background-size: cover;
        background-position: center;
        min-height: 70vh;
        display:flex;
        align-items:center;
        position:relative;
      }
      .hero::after{
        content:"";
        position:absolute;
        inset:0;
        background: linear-gradient(180deg, rgba(0,0,0,0.35), rgba(0,0,0,0.25));
        z-index:0;
      }
      .hero .hero-inner{
        z-index:2;
      }
      .hero h1{
        color:#fff;
        font-weight:800;
        text-shadow:0 6px 20px rgba(0,0,0,0.35);
      }
      .hero .lead{color: #fffddf; font-size:1.125rem;}

      /* CARDS / MENU */
      .flavor-card img{height:220px; object-fit:cover; border-top-left-radius:.375rem; border-top-right-radius:.375rem;}
      .flavor-card .card-body{background:linear-gradient(180deg, rgba(255,255,255,0.96), #fff);}
      .price-badge{
        position:absolute; top:12px; right:12px;
        background:linear-gradient(180deg,var(--accent),var(--accent-dark));
        color:#7b2b2b; padding:6px 10px; border-radius:20px; font-weight:700; box-shadow:0 6px 18px rgba(0,0,0,0.12);
      }

      /* CAROUSEL */
      .carousel-item img{height:320px; object-fit:cover; border-radius:12px; box-shadow:0 10px 30px rgba(0,0,0,0.12);}

      /* FEATURE BOXES */
      .feature{
        background:linear-gradient(180deg,#fff,#fffefc);
        border-radius:12px; padding:20px; box-shadow:0 6px 20px rgba(0,0,0,0.04);
      }

      /* TESTIMONIALS */
      .testimonial { background: var(--glass); padding:18px; border-radius:12px; backdrop-filter: blur(6px); }

      /* CONTACT */
      #formStatus{font-weight:600;}
      .btn-outline-accent{
        border-color: transparent;
        background: linear-gradient(90deg,var(--accent),var(--accent-dark));
        color:#6b1b1b;
        box-shadow: 0 8px 24px rgba(242,153,166,0.18);
      }

      /* FOOTER */
      footer{background:#302626; color:#fff; font-size:.95rem;}
      .copyright{opacity:0.85;}

      /* small screens */
      @media (max-width:767px){
        .hero{min-height:56vh}
        .flavor-card img{height:180px}
      }

      /* micro interactions */
      .card:hover{transform:translateY(-6px); transition:transform .25s ease;}
      .btn:active{transform:translateY(1px);}
    </style>
  </head>

  <body>
    <!-- NAV -->
    <nav class="navbar navbar-expand-lg navbar-light bg-white sticky-top shadow-sm">
      <div class="container">
        <a class="navbar-brand" href="#">Lokesh IceLux</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navCollapse">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navCollapse">
          <ul class="navbar-nav ms-auto align-items-lg-center">
            <li class="nav-item"><a class="nav-link active" href="#home">Home</a></li>
            <li class="nav-item"><a class="nav-link" href="#menu">Menu</a></li>
            <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
            <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
            <li class="nav-item ms-3 d-none d-lg-block">
              <a class="btn btn-outline-accent btn-sm" href="#menu"><i class="bi bi-basket"></i> Order Now</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- HERO -->
    <header id="home" class="hero">
      <div class="container hero-inner text-center text-white">
        <div class="row justify-content-center">
          <div class="col-lg-8">
            <h1 class="display-4">Experience Luxury — One Scoop at a Time</h1>
            <p class="lead mt-3">Handcrafted premium ice cream with the finest ingredients from around the world.</p>
            <div class="mt-4">
              <a href="#menu" class="btn btn-outline-light btn-lg me-2">Explore Menu</a>
              <a href="#contact" class="btn btn-light btn-lg text-dark">Book a Tasting</a>
            </div>

            <div class="mt-4 d-flex justify-content-center gap-3">
              <div class="badge bg-white text-dark px-3 py-2" style="border-radius:28px;"><strong>Madagascar Vanilla</strong></div>
              <div class="badge bg-white text-dark px-3 py-2" style="border-radius:28px;"><strong>Belgian Dark</strong></div>
              <div class="badge bg-white text-dark px-3 py-2" style="border-radius:28px;"><strong>Seasonal: Mango</strong></div>
            </div>
          </div>
        </div>
      </div>
    </header>

    <!-- BEST SELLERS CAROUSEL -->
    <section class="py-5">
      <div class="container">
        <div class="d-flex justify-content-between align-items-center mb-4">
          <h2 class="mb-0">Best Sellers</h2>
          <small class="text-muted">Loved by customers</small>
        </div>

        <div id="bestSellers" class="carousel slide" data-bs-ride="carousel">
          <div class="carousel-inner">
            <div class="carousel-item active">
              <div class="row g-3 align-items-center">
                <div class="col-md-5">
                  <img src="c:\Users\LOKESH\Downloads\chocolate-truffle-ice-cream-recipe-11-of-18-1024x1536.jpg" class="d-block w-100" alt="Chocolate Truffle">
                </div>
                <div class="col-md-7">
                  <h3>Chocolate Truffle</h3>
                  <p class="text-muted">Velvety Belgian dark chocolate with delicate truffle shards and cocoa dust — a decadent classic.</p>
                  <div class="d-flex gap-3 align-items-center">
                    <div class="fs-4 fw-bold">₹199 / scoop</div>
                    <button class="btn btn-outline-accent">Add to Cart</button>
                    <button class="btn btn-outline-secondary">Quick View</button>
                  </div>
                </div>
              </div>
            </div>

            <div class="carousel-item">
              <div class="row g-3 align-items-center">
                <div class="col-md-5">
                  <img src="c:\Users\LOKESH\Downloads\vanilla-bean-ice-cream-2.jpg" class="d-block w-100" alt="Vanilla Bean">
                </div>
                <div class="col-md-7">
                  <h3>Vanilla Bean Reserve</h3>
                  <p class="text-muted">Made with Madagascan vanilla beans — pure, aromatic, and luxuriously smooth.</p>
                  <div class="d-flex gap-3 align-items-center">
                    <div class="fs-4 fw-bold">₹169 / scoop</div>
                    <button class="btn btn-outline-accent">Add to Cart</button>
                    <button class="btn btn-outline-secondary">Quick View</button>
                  </div>
                </div>
              </div>
            </div>

            <div class="carousel-item">
              <div class="row g-3 align-items-center">
                <div class="col-md-5">
                  <img src="c:\Users\LOKESH\Downloads\strawberry;lkjhgfd.jpeg" class="d-block w-100" alt="Strawberry Royale">
                </div>
                <div class="col-md-7">
                  <h3>Strawberry Royale</h3>
                  <p class="text-muted">Fresh strawberry purée folded into creamy base, topped with strawberry glaze.</p>
                  <div class="d-flex gap-3 align-items-center">
                    <div class="fs-4 fw-bold">₹179 / scoop</div>
                    <button class="btn btn-outline-accent">Add to Cart</button>
                    <button class="btn btn-outline-secondary">Quick View</button>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <button class="carousel-control-prev" type="button" data-bs-target="#bestSellers" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button class="carousel-control-next" type="button" data-bs-target="#bestSellers" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
    </section>

    <!-- MENU -->
    <section id="menu" class="py-5 bg-light">
      <div class="container">
        <h2 class="text-center mb-4">Lokesh premium ice cream Flavours</h2>
        <p class="text-center text-muted mb-5">Handcrafted flavors selected for a premium tasting experience.</p>

        <div class="row g-4">
          <div class="col-md-4">
            <div class="card flavor-card h-100 shadow-sm position-relative">
              <div class="price-badge">₹199</div>
              <img src="c:\Users\LOKESH\Downloads\chocolate-truffle-ice-cream-recipe-11-of-18-1024x1536.jpg" class="card-img-top" alt="Chocolate Truffle">
              <div class="card-body text-center">
                <h5 class="card-title">Chocolate Truffle</h5>
                <p class="card-text text-muted">Belgian chocolate, truffle shards, silky texture.</p>
                <div class="d-flex justify-content-center gap-2">
                  <button class="btn btn-outline-accent btn-sm">Add</button>
                  <button class="btn btn-sm btn-outline-secondary">Details</button>
                </div>
              </div>
            </div>
          </div>

          <div class="col-md-4">
            <div class="card flavor-card h-100 shadow-sm position-relative">
              <div class="price-badge">₹169</div>
              <img src="c:\Users\LOKESH\Downloads\vanilla-bean-ice-cream-2.jpg" class="card-img-top" alt="Vanilla Bean">
              <div class="card-body text-center">
                <h5 class="card-title">Vanilla Bean</h5>
                <p class="card-text text-muted">Madagascar vanilla seeds, pure and aromatic.</p>
                <div class="d-flex justify-content-center gap-2">
                  <button class="btn btn-outline-accent btn-sm">Add</button>
                  <button class="btn btn-sm btn-outline-secondary">Details</button>
                </div>
              </div>
            </div>
          </div>

          <div class="col-md-4">
            <div class="card flavor-card h-100 shadow-sm position-relative">
              <div class="price-badge">₹179</div>
              <img src="c:\Users\LOKESH\Downloads\strawberry;lkjhgfd.jpeg" class="card-img-top" alt="Strawberry Royale">
              <div class="card-body text-center">
                <h5 class="card-title">Strawberry Royale</h5>
                <p class="card-text text-muted">Fresh strawberries & strawberry glaze.</p>
                <div class="d-flex justify-content-center gap-2">
                  <button class="btn btn-outline-accent btn-sm">Add</button>
                  <button class="btn btn-sm btn-outline-secondary">Details</button>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- categories -->
        <div class="mt-5">
          <div class="row g-3">
            <div class="col-md-4">
              <div class="feature">
                <h5><i class="bi bi-check2-circle me-2 text-success"></i>Premium Ingredients</h5>
                <p class="mb-0 text-muted">Madagascar vanilla, Belgian chocolate, Italian pistachios and fresh fruits.</p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature">
                <h5><i class="bi bi-snow me-2 text-info"></i>Small Batch Crafting</h5>
                <p class="mb-0 text-muted">Every batch is made in small quantities to ensure freshness.</p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="feature">
                <h5><i class="bi bi-leaf me-2 text-success"></i>Vegan Options</h5>
                <p class="mb-0 text-muted">Seasonal dairy-free flavors made from coconut & almond bases.</p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="py-5">
      <div class="container">
        <h2 class="text-center mb-4">About IceLux</h2>
        <p class="text-center mx-auto" style="max-width:800px; color:var(--muted);">
          IceLux is dedicated to crafting premium ice creams using the finest ingredients from around the world.
          We combine culinary technique, passion, and top-tier ingredients to produce flavors that linger in your memory.
        </p>

        <div class="row align-items-center mt-4 g-4">
          <div class="col-md-6">
            <ul style="max-width:600px; margin:auto; color:var(--muted);">
              <li>Madagascar Vanilla Beans</li>
              <li>Belgian Dark Chocolate</li>
              <li>Fresh Strawberry Puree</li>
              <li>Italian Pistachios</li>
              <li>Natural Honey & Herbs</li>
            </ul>
          </div>
          <div class="col-md-6">
            <div class="card p-3 shadow-sm">
              <h5 class="fw-bold">Our Mission</h5>
              <p class="mb-0 text-muted">To deliver a luxurious tasting experience using natural, artisanal ingredients and responsible sourcing.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="py-5 bg-light">
      <div class="container">
        <h3 class="text-center mb-4">What Customers Say</h3>
        <div class="row g-3 justify-content-center">
          <div class="col-md-4">
            <div class="testimonial text-center">
              <div class="mb-2"><strong>Bhanu</strong></div>
              <p class="mb-1 text-muted">"The Chocolate Truffle is heavenly — decadent and smooth!"</p>
              <div class="text-warning">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="testimonial text-center">
              <div class="mb-2"><strong>Ramesh</strong></div>
              <p class="mb-1 text-muted">"Amazing flavors and the texture is perfect. Highly recommend."</p>
              <div class="text-warning">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="testimonial text-center">
              <div class="mb-2"><strong>suresh</strong></div>
              <p class="mb-1 text-muted">"Best premium ice cream I've had in the city. Lovely experience."</p>
              <div class="text-warning">⭐⭐⭐⭐⭐</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="py-5">
      <div class="container">
        <h2 class="text-center mb-4">Contact & Bookings</h2>
        <div class="row justify-content-center">
          <div class="col-lg-8">
            <form id="contactForm" class="row g-3 needs-validation" novalidate>
              <div class="col-md-6">
                <label class="form-label visually-hidden" for="name">Name</label>
                <input id="name" type="text" class="form-control form-control-lg" placeholder="Name" required>
                <div class="invalid-feedback">Please enter your name.</div>
              </div>

              <div class="col-md-6">
                <label class="form-label visually-hidden" for="email">Email</label>
                <input id="email" type="email" class="form-control form-control-lg" placeholder="Email" required>
                <div class="invalid-feedback">Please enter a valid email.</div>
              </div>

              <div class="col-12">
                <label class="form-label visually-hidden" for="message">Message</label>
                <textarea id="message" class="form-control" placeholder="Tell us about your booking or message" rows="4" required></textarea>
                <div class="invalid-feedback">Please enter a message.</div>
              </div>

              <div class="col-12 text-center">
                <button id="submitBtn" type="submit" class="btn btn-outline-accent btn-lg">Send Message</button>
                <span id="formStatus" class="ms-3"></span>
              </div>
            </form>

            <div class="text-center mt-4 text-muted">
              Or reach us at: <a href="tel:+6305808441">+6305808441</a> • <a href="mailto:uppariulokesh@gmail.com">uppariulokesh@gmail.com</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-4">
      <div class="container d-flex justify-content-between align-items-center">
        <div>
          <strong>IceLux</strong> • Premium Ice Cream
        </div>
        <div class="text-end">
          <small class="copyright">&copy; <span id="year"></span> IceLux</small>
        </div>
      </div>
    </footer>

    <!-- Bootstrap JS bundle -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

    <script>
      // Set year
      document.getElementById('year').textContent = new Date().getFullYear();

      // Simple client-side form handling (simulates submit + stores to localStorage)
      (function(){
        const form = document.getElementById('contactForm');
        const status = document.getElementById('formStatus');
        const submitBtn = document.getElementById('submitBtn');

        form.addEventListener('submit', function(e){
          e.preventDefault();
          if (!form.checkValidity()) {
            form.classList.add('was-validated');
            return;
          }

          // Simulate async submit
          submitBtn.disabled = true;
          submitBtn.textContent = "Sending...";

          const data = {
            name: document.getElementById('name').value.trim(),
            email: document.getElementById('email').value.trim(),
            message: document.getElementById('message').value.trim(),
            time: (new Date()).toISOString()
          };

          // Save to localStorage (demo) - replace with actual endpoint in production
          const saved = JSON.parse(localStorage.getItem('icelux_contacts') || '[]');
          saved.push(data);
          localStorage.setItem('icelux_contacts', JSON.stringify(saved));

          setTimeout(() => {
            submitBtn.disabled = false;
            submitBtn.textContent = "Send Message";
            form.reset();
            form.classList.remove('was-validated');
            status.textContent = "Message sent — we'll contact you soon!";
            status.style.color = "green";

            // hide message after 5s
            setTimeout(()=>{ status.textContent = ""; }, 5000);
          }, 700);
        });

      })();

      // Accessibility: enable keyboard focus visible outlines
      document.addEventListener('keyup', (e) => {
        if (e.key === 'Tab') document.body.classList.add('user-is-tabbing');
      });
    </script>

  </body>
</html>
