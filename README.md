<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VOWEL VMS · CompuLynx</title>
  <!-- Google Font & Font Awesome for clean icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f4f7fc;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
      line-height: 1.5;
      color: #1e293b;
    }

    .card {
      max-width: 1200px;
      width: 100%;
      background: #ffffff;
      border-radius: 40px;
      box-shadow: 0 30px 60px -20px rgba(0, 20, 50, 0.25), 0 12px 30px -10px rgba(0, 0, 0, 0.05);
      overflow: hidden;
      transition: all 0.2s ease;
      padding: 2.8rem 3rem;
    }

    @media (max-width: 768px) {
      .card {
        padding: 2rem 1.5rem;
      }
    }

    /* header section */
    .brand-header {
      display: flex;
      flex-wrap: wrap;
      align-items: baseline;
      justify-content: space-between;
      margin-bottom: 1.2rem;
      border-bottom: 2px solid #eef2f6;
      padding-bottom: 1.6rem;
    }

    .brand-title {
      display: flex;
      align-items: center;
      gap: 0.65rem;
    }

    .brand-title i {
      font-size: 2.4rem;
      color: #2563eb;
      background: #dbeafe;
      padding: 0.5rem;
      border-radius: 20px;
    }

    .brand-title h1 {
      font-size: 2.2rem;
      font-weight: 800;
      letter-spacing: -0.02em;
      background: linear-gradient(145deg, #0b2b5c, #1e4a7a);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .brand-title h1 span {
      font-weight: 300;
      background: none;
      -webkit-text-fill-color: #475569;
      color: #475569;
      font-size: 1.6rem;
      margin-left: 0.25rem;
    }

    .tagline {
      background: #eef2ff;
      padding: 0.45rem 1.2rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 0.9rem;
      color: #1e3a8a;
      letter-spacing: 0.3px;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      white-space: nowrap;
    }

    .tagline i {
      font-size: 0.9rem;
      color: #2563eb;
    }

    @media (max-width: 700px) {
      .brand-header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.8rem;
      }
      .tagline {
        white-space: normal;
      }
    }

    /* main description */
    .description {
      margin: 1.8rem 0 2.4rem 0;
      background: #f8fafc;
      padding: 1.8rem 2rem;
      border-radius: 28px;
      border-left: 6px solid #2563eb;
    }

    .description p {
      font-size: 1.1rem;
      font-weight: 400;
      color: #1e293b;
      max-width: 85%;
    }

    .description strong {
      color: #0b2b5c;
      font-weight: 700;
    }

    .region-badge {
      display: inline-flex;
      flex-wrap: wrap;
      gap: 0.5rem 1rem;
      margin-top: 1rem;
      background: #ffffff;
      padding: 0.6rem 1.4rem;
      border-radius: 60px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.02);
      font-weight: 500;
      font-size: 0.95rem;
      color: #1e3a8a;
    }

    .region-badge i {
      margin-right: 0.3rem;
      color: #2563eb;
    }

    .region-badge span {
      background: #e6edfa;
      padding: 0.1rem 0.9rem;
      border-radius: 40px;
      font-weight: 600;
    }

    @media (max-width: 600px) {
      .description p {
        max-width: 100%;
        font-size: 1rem;
      }
    }

    /* feature grid */
    .feature-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.8rem;
      margin: 2.8rem 0 2rem 0;
    }

    @media (max-width: 900px) {
      .feature-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 550px) {
      .feature-grid {
        grid-template-columns: 1fr;
      }
    }

    .feature-item {
      background: #fafcff;
      padding: 1.8rem 1.5rem;
      border-radius: 28px;
      transition: 0.2s ease;
      border: 1px solid #e9eef4;
      box-shadow: 0 4px 10px -8px rgba(0,0,0,0.02);
    }

    .feature-item:hover {
      background: #ffffff;
      border-color: #bdd3f0;
      box-shadow: 0 12px 24px -12px rgba(37, 99, 235, 0.12);
      transform: translateY(-3px);
    }

    .feature-icon {
      background: #dbeafe;
      width: 56px;
      height: 56px;
      border-radius: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1.2rem;
    }

    .feature-icon i {
      font-size: 2rem;
      color: #1e4a7a;
    }

    .feature-item h3 {
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 0.6rem;
      letter-spacing: -0.02em;
      color: #0b2b5c;
    }

    .feature-item p {
      color: #334155;
      font-weight: 400;
      font-size: 0.98rem;
      line-height: 1.5;
    }

    /* bottom row: extra info + CTA */
    .bottom-section {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      margin-top: 2.4rem;
      padding-top: 2rem;
      border-top: 2px solid #eef2f6;
    }

    .powered {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 500;
      color: #334155;
      background: #f1f5f9;
      padding: 0.5rem 1.4rem;
      border-radius: 60px;
      font-size: 0.95rem;
    }

    .powered i {
      color: #2563eb;
      font-size: 1.2rem;
    }

    .powered strong {
      font-weight: 700;
      color: #0b2b5c;
    }

    .cta-button {
      background: #0b2b5c;
      color: white;
      border: none;
      padding: 0.8rem 2.2rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 1rem;
      display: inline-flex;
      align-items: center;
      gap: 0.8rem;
      transition: 0.15s ease;
      box-shadow: 0 6px 14px -6px rgba(11, 43, 92, 0.25);
      cursor: default;
    }

    .cta-button i {
      font-size: 1.1rem;
    }

    .cta-button:hover {
      background: #1e4a7a;
      box-shadow: 0 10px 20px -10px #1e4a7a70;
      transform: scale(1.01);
    }

    @media (max-width: 600px) {
      .bottom-section {
        flex-direction: column;
        align-items: flex-start;
        gap: 1.2rem;
      }
    }

    /* small extras */
    .accent-dot {
      display: inline-block;
      width: 10px;
      height: 10px;
      background: #2563eb;
      border-radius: 20px;
      margin-right: 0.6rem;
    }

    .subnote {
      color: #64748b;
      font-size: 0.9rem;
      margin-top: 1.5rem;
      text-align: right;
      border-top: 1px solid #eef2f6;
      padding-top: 1.5rem;
      letter-spacing: 0.2px;
    }

    .subnote i {
      margin: 0 0.2rem;
      color: #2563eb;
    }
  </style>
</head>
<body>
  <div class="card">
    
    <!-- Header: VOWEL VMS + CompuLynx -->
    <div class="brand-header">
      <div class="brand-title">
        <i class="fas fa-building-user"></i>
        <h1>VOWEL <span>VMS</span></h1>
      </div>
      <div class="tagline">
        <i class="fas fa-arrow-right"></i> Visitor Official Welcome Management
      </div>
    </div>

    <!-- Description & region -->
    <div class="description">
      <p>
        <strong>VOWEL</strong> (Visitors’ Official Welcome) is a digital visitor management system by <strong>CompuLynx</strong>.
        It replaces traditional logbooks with a fast, secure, and paperless front-desk experience.
        Deployed across commercial and residential premises in <strong>Kenya, Uganda, and Tanzania</strong>, 
        it ensures seamless check-ins, instant visitor tracking, and digital records.
      </p>
      <div class="region-badge">
        <i class="fas fa-map-pin"></i> Active in 
        <span><i class="fas fa-flag"></i> Kenya</span>
        <span><i class="fas fa-flag"></i> Uganda</span>
        <span><i class="fas fa-flag"></i> Tanzania</span>
        <i class="fas fa-cloud" style="margin-left: 0.6rem;"></i> cloud–native
      </div>
    </div>

    <!-- 3 core features -->
    <div class="feature-grid">
      <div class="feature-item">
        <div class="feature-icon"><i class="fas fa-pen-to-square"></i></div>
        <h3>Paperless Check‑ins</h3>
        <p>Self‑registration or front‑desk log‑in in seconds. Generates a fast digital footprint, eliminates paper clutter.</p>
      </div>
      <div class="feature-item">
        <div class="feature-icon"><i class="fas fa-shield-halved"></i></div>
        <h3>Access Control</h3>
        <p>Integrates into your facility's security infrastructure, enhancing visitor experiences and physical safety.</p>
      </div>
      <div class="feature-item">
        <div class="feature-icon"><i class="fas fa-database"></i></div>
        <h3>Cloud & Digital Records</h3>
        <p>Creates secure, searchable databases for better building transparency, compliance, and audit readiness.</p>
      </div>
    </div>

    <!-- bottom: powered + CTA -->
    <div class="bottom-section">
      <div class="powered">
        <i class="fas fa-microchip"></i> 
        <span>Powered by <strong>CompuLynx</strong> · East Africa</span>
      </div>
      <div class="cta-button">
        <i class="fas fa-arrow-right-to-bracket"></i> 
        <span>Upgrade your reception</span>
        <i class="fas fa-chevron-right" style="font-size: 0.8rem; opacity: 0.8;"></i>
      </div>
    </div>

    <!-- extra note: transparent & professional -->
    <div class="subnote">
      <i class="fas fa-circle-check"></i>  paperless · secure · real‑time 
      <span style="margin: 0 0.6rem;">|</span> 
      <i class="fas fa-rotate-right"></i>  instant visitor tracking 
      <span style="margin: 0 0.6rem;">|</span> 
      <i class="fas fa-shield"></i>  enterprise‑grade
    </div>
  </div>
</body>
</html>
