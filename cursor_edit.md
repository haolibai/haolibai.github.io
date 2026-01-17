# 学术现代主页设计
_Exported on 1/17/2026 at 17:52:28 GMT+8 from Cursor (2.3.34)_

---

**User**

帮我改善一下这个网页观感，风格是学术，简洁，现代的；请创建一个新的主页html文件

---

**Cursor**

让我先查看现有的网页内容和样式，了解当前的结构和信息。

现在我了解了网页的完整内容。让我为您创建一个现代、简洁、学术风格的新主页。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Haoli Bai (柏昊立)</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Source+Sans+3:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --color-bg: #faf9f7;
      --color-text: #1a1a1a;
      --color-text-secondary: #4a4a4a;
      --color-accent: #8b4513;
      --color-accent-light: #c4956a;
      --color-border: #e0dcd4;
      --color-card-bg: #ffffff;
      --color-tag: #f5f0eb;
      --font-serif: 'Cormorant Garamond', Georgia, serif;
      --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
      --max-width: 860px;
      --spacing-unit: 1rem;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-sans);
      font-size: 16px;
      line-height: 1.7;
      color: var(--color-text);
      background: var(--color-bg);
      -webkit-font-smoothing: antialiased;
    }

    /* Subtle background pattern */
    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(circle at 20% 20%, rgba(139, 69, 19, 0.03) 0%, transparent 50%),
        radial-gradient(circle at 80% 80%, rgba(139, 69, 19, 0.02) 0%, transparent 50%);
      pointer-events: none;
      z-index: -1;
    }

    .container {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 calc(var(--spacing-unit) * 1.5);
    }

    /* Header */
    header {
      padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
      animation: fadeInUp 0.8s ease-out;
    }

    .header-content {
      display: flex;
      gap: calc(var(--spacing-unit) * 3);
      align-items: flex-start;
    }

    .profile-image {
      width: 180px;
      height: 180px;
      border-radius: 8px;
      object-fit: cover;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
      flex-shrink: 0;
      transition: transform 0.3s ease;
    }

    .profile-image:hover {
      transform: translateY(-4px);
    }

    .header-info {
      flex: 1;
    }

    .header-info h1 {
      font-family: var(--font-serif);
      font-size: 2.5rem;
      font-weight: 600;
      color: var(--color-text);
      margin-bottom: 0.5rem;
      letter-spacing: -0.02em;
    }

    .affiliation {
      font-size: 1.1rem;
      color: var(--color-text-secondary);
      margin-bottom: 0.25rem;
    }

    .location {
      font-size: 0.95rem;
      color: var(--color-text-secondary);
      margin-bottom: 1rem;
    }

    .contact-email {
      font-size: 0.95rem;
      color: var(--color-text-secondary);
      margin-bottom: 1.25rem;
    }

    .contact-email strong {
      color: var(--color-text);
    }

    .social-links {
      display: flex;
      gap: 0.75rem;
    }

    .social-links a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 36px;
      height: 36px;
      border-radius: 6px;
      background: var(--color-card-bg);
      border: 1px solid var(--color-border);
      transition: all 0.2s ease;
    }

    .social-links a:hover {
      background: var(--color-accent);
      border-color: var(--color-accent);
      transform: translateY(-2px);
    }

    .social-links a:hover img {
      filter: brightness(0) invert(1);
    }

    .social-links img {
      width: 20px;
      height: 20px;
      transition: filter 0.2s ease;
    }

    /* Navigation */
    nav {
      position: sticky;
      top: 0;
      background: rgba(250, 249, 247, 0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--color-border);
      z-index: 100;
      margin-bottom: calc(var(--spacing-unit) * 2);
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 0.25rem;
      padding: 0.75rem 0;
      overflow-x: auto;
      -webkit-overflow-scrolling: touch;
    }

    nav a {
      display: block;
      padding: 0.5rem 1rem;
      font-size: 0.9rem;
      font-weight: 500;
      color: var(--color-text-secondary);
      text-decoration: none;
      border-radius: 6px;
      transition: all 0.2s ease;
      white-space: nowrap;
    }

    nav a:hover {
      color: var(--color-accent);
      background: var(--color-tag);
    }

    /* Sections */
    section {
      margin-bottom: calc(var(--spacing-unit) * 3);
      animation: fadeInUp 0.6s ease-out backwards;
    }

    section:nth-child(2) { animation-delay: 0.1s; }
    section:nth-child(3) { animation-delay: 0.15s; }
    section:nth-child(4) { animation-delay: 0.2s; }
    section:nth-child(5) { animation-delay: 0.25s; }
    section:nth-child(6) { animation-delay: 0.3s; }

    h2 {
      font-family: var(--font-serif);
      font-size: 1.5rem;
      font-weight: 600;
      color: var(--color-text);
      margin-bottom: calc(var(--spacing-unit) * 1.25);
      padding-bottom: 0.5rem;
      border-bottom: 2px solid var(--color-accent-light);
      display: inline-block;
    }

    /* Bio */
    .bio {
      font-size: 1rem;
      line-height: 1.8;
      color: var(--color-text-secondary);
    }

    .bio a {
      color: var(--color-accent);
      text-decoration: none;
      border-bottom: 1px solid transparent;
      transition: border-color 0.2s ease;
    }

    .bio a:hover {
      border-bottom-color: var(--color-accent);
    }

    .hiring-notice {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: linear-gradient(135deg, #fff7ed, #fef3e2);
      border: 1px solid #f5d0a9;
      border-radius: 8px;
      padding: 0.75rem 1rem;
      margin-top: 1rem;
      font-size: 0.95rem;
    }

    .hiring-notice .fire {
      font-size: 1.1rem;
    }

    /* News */
    .news-list {
      list-style: none;
    }

    .news-item {
      display: flex;
      gap: 1rem;
      padding: 1rem 0;
      border-bottom: 1px solid var(--color-border);
    }

    .news-item:last-child {
      border-bottom: none;
    }

    .news-date {
      flex-shrink: 0;
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--color-accent);
      background: var(--color-tag);
      padding: 0.25rem 0.75rem;
      border-radius: 4px;
      height: fit-content;
    }

    .news-content {
      font-size: 0.95rem;
      color: var(--color-text-secondary);
      line-height: 1.6;
    }

    .news-content a {
      color: var(--color-accent);
      text-decoration: none;
    }

    .news-content a:hover {
      text-decoration: underline;
    }

    /* Publications */
    .pub-note {
      font-size: 0.9rem;
      color: var(--color-text-secondary);
      font-style: italic;
      margin-bottom: 1.5rem;
    }

    .publication {
      background: var(--color-card-bg);
      border: 1px solid var(--color-border);
      border-radius: 10px;
      padding: 1.25rem 1.5rem;
      margin-bottom: 1rem;
      transition: all 0.2s ease;
    }

    .publication:hover {
      border-color: var(--color-accent-light);
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
    }

    .pub-title {
      font-weight: 600;
      color: var(--color-text);
      margin-bottom: 0.5rem;
      line-height: 1.4;
    }

    .pub-title a {
      color: var(--color-text);
      text-decoration: none;
      transition: color 0.2s ease;
    }

    .pub-title a:hover {
      color: var(--color-accent);
    }

    .pub-authors {
      font-size: 0.9rem;
      color: var(--color-text-secondary);
      margin-bottom: 0.5rem;
      line-height: 1.5;
    }

    .pub-venue {
      font-size: 0.9rem;
      font-style: italic;
      color: var(--color-text-secondary);
      margin-bottom: 0.5rem;
    }

    .pub-links {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
    }

    .pub-links a {
      font-size: 0.8rem;
      font-weight: 500;
      color: var(--color-accent);
      text-decoration: none;
      padding: 0.25rem 0.75rem;
      background: var(--color-tag);
      border-radius: 4px;
      transition: all 0.2s ease;
    }

    .pub-links a:hover {
      background: var(--color-accent);
      color: white;
    }

    /* Talks */
    .talks-list {
      list-style: none;
    }

    .talk-item {
      padding: 1rem 0;
      border-bottom: 1px solid var(--color-border);
      font-size: 0.95rem;
      color: var(--color-text-secondary);
    }

    .talk-item:last-child {
      border-bottom: none;
    }

    .talk-item a {
      color: var(--color-accent);
      text-decoration: none;
    }

    .talk-item a:hover {
      text-decoration: underline;
    }

    /* Projects */
    .project {
      background: var(--color-card-bg);
      border: 1px solid var(--color-border);
      border-radius: 10px;
      padding: 1.25rem 1.5rem;
      margin-bottom: 1rem;
    }

    .project-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 0.75rem;
    }

    .project-title {
      font-weight: 600;
      color: var(--color-text);
    }

    .project-links {
      display: flex;
      gap: 0.5rem;
    }

    .project-links a {
      font-size: 0.8rem;
      color: var(--color-accent);
      text-decoration: none;
      padding: 0.2rem 0.6rem;
      background: var(--color-tag);
      border-radius: 4px;
    }

    .project-links a:hover {
      background: var(--color-accent);
      color: white;
    }

    .project-desc {
      font-size: 0.95rem;
      color: var(--color-text-secondary);
      line-height: 1.6;
    }

    /* Services */
    .service-category {
      margin-bottom: 1rem;
    }

    .service-title {
      font-weight: 600;
      color: var(--color-text);
      font-size: 0.95rem;
      margin-bottom: 0.25rem;
    }

    .service-content {
      font-size: 0.95rem;
      color: var(--color-text-secondary);
    }

    /* Awards & Experience */
    .timeline-item {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      padding: 0.75rem 0;
      border-bottom: 1px solid var(--color-border);
      font-size: 0.95rem;
    }

    .timeline-item:last-child {
      border-bottom: none;
    }

    .timeline-title {
      color: var(--color-text);
    }

    .timeline-title a {
      color: var(--color-accent);
      text-decoration: none;
    }

    .timeline-title a:hover {
      text-decoration: underline;
    }

    .timeline-year {
      color: var(--color-text-secondary);
      flex-shrink: 0;
      margin-left: 1rem;
    }

    /* Footer */
    footer {
      margin-top: calc(var(--spacing-unit) * 4);
      padding: calc(var(--spacing-unit) * 2) 0;
      border-top: 1px solid var(--color-border);
      text-align: center;
    }

    .footer-content {
      font-size: 0.85rem;
      color: var(--color-text-secondary);
      margin-bottom: 1.5rem;
    }

    .footer-content a {
      color: var(--color-accent);
      text-decoration: none;
    }

    .visitor-map {
      max-width: 300px;
      margin: 0 auto;
    }

    /* Animations */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Responsive */
    @media (max-width: 768px) {
      .header-content {
        flex-direction: column;
        align-items: center;
        text-align: center;
      }

      .header-info h1 {
        font-size: 2rem;
      }

      .social-links {
        justify-content: center;
      }

      nav ul {
        justify-content: flex-start;
      }

      .timeline-item {
        flex-direction: column;
        gap: 0.25rem;
      }

      .timeline-year {
        margin-left: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="header-content">
        <img src="img/square_light.jpg" alt="Haoli Bai" class="profile-image">
        <div class="header-info">
          <h1>Haoli Bai (柏昊立)</h1>
          <p class="affiliation">Researcher, Huawei Hong Kong Research Center</p>
          <p class="location">Hong Kong SAR, China</p>
          <p class="contact-email"><strong>Email:</strong> haolibai [at] gmail.com</p>
          <div class="social-links">
            <a href="https://scholar.google.com/citations?user=pk7jX3gAAAAJ&hl=zh-CN" title="Google Scholar">
              <img src="./img/google_scholar.png" alt="Google Scholar">
            </a>
            <a href="https://dblp.org/pid/195/9712.html" title="DBLP">
              <img src="./img/dblp.png" alt="DBLP">
            </a>
            <a href="https://github.com/haolibai" title="GitHub">
              <img src="./img/github_s.jpg" alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/baihaoli-407136142/" title="LinkedIn">
              <img src="./img/LinkedIn_s.png" alt="LinkedIn">
            </a>
          </div>
        </div>
      </div>
    </header>

    <nav>
      <div class="container">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#publications">Publications</a></li>
          <li><a href="#talks">Talks</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#awards">Awards</a></li>
          <li><a href="#experience">Experience</a></li>
        </ul>
      </div>
    </nav>

    <main>
      <section id="about">
        <h2>About</h2>
        <div class="bio">
          <p>I am currently a researcher at the Language Model Lab, Huawei Hong Kong Research Center. I obtained my Ph.D. degree from The Chinese University of Hong Kong supervised by <a href="https://www.cse.cuhk.edu.hk/lyu/">Prof. Michael R. Lyu</a> and <a href="https://www.cse.cuhk.edu.hk/irwin.king/">Prof. Irwin King</a>, and the B.Eng. Degree from Yingcai Honors College of University of Electronic Science and Technology.</p>
          <p style="margin-top: 1rem;">Our team's effort is on large language models with topics spanning from pre-training, post-training, to agentic AI (e.g., deep research and coding agent). I am also an experienced researcher in LLM efficiency, e.g., compression and acceleration of LLMs.</p>
          <div class="hiring-notice">
            <span class="fire">🔥</span>
            <span><strong>[Hiring]</strong> We are constantly looking for full-time researchers and research interns with solid algorithm or system background (Base: HK or Shenzhen). Please connect by E-Mail.</span>
          </div>
        </div>
      </section>

      <section id="news">
        <h2>News</h2>
        <ul class="news-list">
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">We will present the tutorial "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">Tutorial website</a></span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">I will give a talk on "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG 2025</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-9</span>
            <span class="news-content">Our paper <a href="https://arxiv.org/abs/2505.24680">"A Simple Linear Patch Revives Layer-Pruned Large Language Models"</a> is accepted by NeurIPS 2025.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-7</span>
            <span class="news-content">🔥 Our paper <a href="https://arxiv.org/abs/2504.04823v1">"Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models"</a> is accepted by COLM 2025. It was on the top-10 trending list on <a href="https://www.alphaxiv.org/abs/2504.04823">alphaXiv</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-4</span>
            <span class="news-content">I will serve as the Area Chair for NeurIPS 2025.</span>
          </li>
        </ul>
      </section>

      <section id="publications">
        <h2>Selected Publications</h2>
        <p class="pub-note">*: Equal contribution; #: Corresponding author; +: Project lead</p>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2505.24680">A Simple Linear Patch Revives Layer-Pruned Large Language Models</a>
          </div>
          <div class="pub-authors">Xinrui Chen, <strong>Haoli Bai</strong><sup>#+</sup>, Tao Yuan, Ruikang Liu, Kang Zhao, Xianzhi Yu, Lu Hou, Tian Guan, Yonghong He, Chun Yuan<sup>#</sup></div>
          <div class="pub-venue">Proceedings of the 39th conference on Neural Information Processing Systems (NeurIPS), 2025.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2504.04823v1">Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models</a>
          </div>
          <div class="pub-authors">Ruikang Liu<sup>*</sup>, Yuxuan Sun<sup>*</sup>, Manyi Zhang<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Xianzhi Yu, Tiezheng Yu, Chun Yuan, Lu Hou<sup>#</sup></div>
          <div class="pub-venue">Conference on Language Modeling (COLM), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/Quantized-Reasoning-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2410.09426">FlatQuant: Flatness Matters for LLM Quantization</a>
          </div>
          <div class="pub-authors">Yuxuan Sun<sup>*</sup>, Ruikang Liu<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Han Bao, Kang Zhao, Yuening Li, Jiaxin Hu, Xianzhi Yu, Lu Hou, Chun Yuan, Xin Jiang, Wulong Liu, Jun Yao</div>
          <div class="pub-venue">International Conference on Machine Learning (ICML), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/FlatQuant">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://aclanthology.org/2024.naacl-long.264.pdf">Visually Guided Generative Text-Layout Pre-training for Document Intelligence</a>
          </div>
          <div class="pub-authors">Zhiming Mao, <strong>Haoli Bai</strong><sup>#+</sup>, Lu Hou, Lifeng Shang, Xin Jiang, Qun Liu, Kam-Fai Wong</div>
          <div class="pub-venue">The North American Chapter of the Association for Computational Linguistics (NAACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/Veason-silverbullet/ViTLP">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.01241">IntactKV: Improving Large Language Model Quantization by Keeping Pivot Tokens Intact</a>
          </div>
          <div class="pub-authors">Ruikang Liu, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Yuening Li, Han Gao, Zhengzhuo Xu, Lu Hou, Jun Yao, Chun Yuan</div>
          <div class="pub-venue">Findings of Annual Meeting of the Association for Computational Linguistics (ACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/IntactKV">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.07839v1">MoPE-CLIP: Structured Pruning for Efficient Vision-Language Models with Module-wise Pruning Error Metric</a>
          </div>
          <div class="pub-authors">Haokun Lin, <strong>Haoli Bai</strong><sup>+</sup>, Zhili Liu, Lu Hou, Muyi Sun, Linqi Song, Ying Wei, Zhenan Sun</div>
          <div class="pub-venue">Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2024.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://openreview.net/forum?id=Tr0lPx9woF">Plug-and-Play: An Efficient Post-training Pruning Method for Large Language Models</a>
          </div>
          <div class="pub-authors">Yingtao Zhang, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Jialin Zhao, Lu Hou, Carlo Vittorio Cannistraci</div>
          <div class="pub-venue">The Twelfth International Conference on Learning Representations (ICLR), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/biomedical-cybernetics/Relative-importance-and-activation-pruning">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2212.09621">Wukong-Reader: Multi-modal Pre-training for Fine-grained Visual Document Understanding</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Zhiguang Liu<sup>*</sup>, Xiaojun Meng<sup>*</sup>, Wentao Li, Shuang Liu, Nian Xie, Rongfu Zheng, Liangwei Wang, Lu Hou, Jiansheng Wei, Xin Jiang, Qun Liu</div>
          <div class="pub-venue">The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <span>Structured Pruning for Efficient Generative Pre-trained Language Models</span>
          </div>
          <div class="pub-authors">Chaofan Tao, Lu Hou<sup>+</sup>, <strong>Haoli Bai</strong><sup>+</sup>, Jiansheng Wei, Xin Jiang, Qun Liu, Ping Luo, Ngai Wong</div>
          <div class="pub-venue">Findings of The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2109.15082.pdf">Towards Efficient Post-training Quantization of Pre-trained Language Models</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Lu Hou, Lifeng Shang, Xin Jiang, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 36th conference on Neural Information Processing Systems (NeurIPS), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2111.09499">Dynamically pruning segformer for efficient semantic segmentation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Hongda Mao, Dinesh Nair</div>
          <div class="pub-venue">IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2012.15701">BinaryBERT: Pushing the Limit of BERT Quantization</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Wei Zhang, Lu Hou, Lifeng Shang, Jing Jin, Xin Jiang, Qun Liu, Michael Lyu, Irwin King</div>
          <div class="pub-venue">The 59th Annual Meeting of the Association for Computational Linguistics (ACL), 2021. <strong>Accepted with scores 5, 5, 4.</strong></div>
          <div class="pub-links">
            <a href="https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/BinaryBERT">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://proceedings.neurips.cc/paper/2020/file/42cd63cb189c30ed03e42ce2c069566c-Paper.pdf">Revisiting Parameter Sharing for Automatic Neural Channel Number Search</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Jiaxing Wang<sup>*</sup>, Jiaxiang Wu, Xupeng Shi, Junzhou Huang, Irwin King, Michael Lyu, Jian Cheng</div>
          <div class="pub-venue">Proceedings of the 34th conference on Neural Information Processing Systems (NeurIPS), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/APS-channel-search">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/1911.09450">Few Shot Network Compression via Cross Distillation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Jiaxiang Wu, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 34th AAAI Conference on Artificial Intelligence (AAAI), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/Cross-Distillation">Code</a>
            <a href="assets/aaai20_poster.pdf">Poster</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://17a11ed1-a-62cb3a1a-s-sites.googlegroups.com/site/nipsts2017/NIPS_2017_TSW_paper_19.pdf">Neural Relational Topic Models for Scientific Article Analysis</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zhuangbin Chen, Michael Lyu, Irwin King, Zenglin Xu</div>
          <div class="pub-venue">Proceedings of The 27th International Conference on Information and Knowledge Management (CIKM), 2018.</div>
          <div class="pub-links">
            <a href="https://github.com/zbchern/Neural-Relational-Topic-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="http://proceedings.mlr.press/v63/bai103.html">Hierarchical Probabilistic Matrix Factorization with Network Topology for Multi-relational Social Network</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zenglin Xu, Bin Liu, Yingming Li</div>
          <div class="pub-venue">Proceedings of The 8th Asian Conference on Machine Learning (ACML), 2016. <strong>Best Student Paper Runner-up</strong>.</div>
        </div>
      </section>

      <section id="talks">
        <h2>Invited Talks</h2>
        <ul class="talks-list">
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="https://www.slai.edu.cn/">SLAI</a>, 2025. <a href="assets/quantization-pruning-public.pdf">[Slide]</a>
          </li>
          <li class="talk-item">
            "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP Tutorial, 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">[Tutorial website]</a>
          </li>
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG</a>, 2025.
          </li>
        </ul>
      </section>

      <section id="projects">
        <h2>Projects</h2>
        <div class="project">
          <div class="project-header">
            <span class="project-title">PocketFlow: An Automated Framework for Compressing and Accelerating DNNs</span>
            <div class="project-links">
              <a href="https://github.com/tencent/PocketFlow">Code</a>
              <a href="https://pocketflow.github.io/">Doc</a>
            </div>
          </div>
          <p class="project-desc">PocketFlow automatically searches for optimal model compression strategies such as network pruning, quantization, knowledge distillation with little human efforts, and also supports TFLite deployment on Android devices. It has collected 2600+ stars and 480+ forks.</p>
        </div>
      </section>

      <section id="services">
        <h2>Services</h2>
        <div class="service-category">
          <div class="service-title">Area Chair</div>
          <div class="service-content">NeurIPS 2025</div>
        </div>
        <div class="service-category">
          <div class="service-title">Senior PC Member</div>
          <div class="service-content">IJCAI 2021</div>
        </div>
        <div class="service-category">
          <div class="service-title">PC Member</div>
          <div class="service-content">ICLR 22-25, ICML 21-25, NeurIPS 20-24, ACL ARR 25, COLM 25, ICCV 25, AAAI 19-21, IJCAI 20</div>
        </div>
        <div class="service-category">
          <div class="service-title">Journal Reviewer</div>
          <div class="service-content">T-PAMI, Neural Networks, etc.</div>
        </div>
      </section>

      <section id="awards">
        <h2>Selected Awards</h2>
        <div class="timeline-item">
          <span class="timeline-title">Excellent Intern, Huawei Noah's Ark Lab</span>
          <span class="timeline-year">2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">AAAI Student Travel Grant</span>
          <span class="timeline-year">2020</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">ACM Student Travel Grant, CIKM</span>
          <span class="timeline-year">2018</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CUHK Postgraduate Student Scholarship</span>
          <span class="timeline-year">2017-2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Best Student Paper Runner-up, ACML</span>
          <span class="timeline-year">2016</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">National Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Tang Lixin Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
      </section>

      <section id="experience">
        <h2>Experience</h2>
        <h3 style="font-family: var(--font-serif); font-size: 1.1rem; margin: 1.5rem 0 0.75rem; color: var(--color-text);">Work Experience</h3>
        <div class="timeline-item">
          <span class="timeline-title">Applied Scientist Intern at <a href="https://www.amazon.jobs/en/business_categories/amazon-devices">Amazon Devices</a></span>
          <span class="timeline-year">2021 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="http://www.noahlab.com.hk/#/home">Huawei Noah's Ark Lab</a></span>
          <span class="timeline-year">2020 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="https://ai.tencent.com/ailab/index.html">Tencent AI Lab</a></span>
          <span class="timeline-year">2018 Summer</span>
        </div>

        <h3 style="font-family: var(--font-serif); font-size: 1.1rem; margin: 1.5rem 0 0.75rem; color: var(--color-text);">Teaching Assistant</h3>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2020 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2019 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI1540: Introduction to C++</span>
          <span class="timeline-year">2018 Fall</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2018 Spring</span>
        </div>
      </section>
    </main>

    <footer>
      <div class="footer-content">
        <p>&copy; <span id="year"></span> Haoli Bai · <a href="#" id="top-link">Back to top ↑</a></p>
      </div>
      <div class="visitor-map">
        <script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=nQLu84viePq1dfXIYnjoGiQxqm-r7hYJeX8f_Oug7fo&cl=ffffff&w=a"></script>
      </div>
    </footer>
  </div>

  <script>
    // Set current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for navigation
    document.querySelectorAll('nav a, #top-link').forEach(link => {
      link.addEventListener('click', function(e) {
        if (this.id === 'top-link') {
          e.preventDefault();
          window.scrollTo({ top: 0, behavior: 'smooth' });
          return;
        }
        const href = this.getAttribute('href');
        if (href.startsWith('#')) {
          e.preventDefault();
          const target = document.querySelector(href);
          if (target) {
            target.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        }
      });
    });

    // Add scroll-based nav highlight
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('nav a');

    function highlightNav() {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 100;
        if (pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });

      navLinks.forEach(link => {
        link.style.color = '';
        link.style.background = '';
        if (link.getAttribute('href') === `#${current}`) {
          link.style.color = '#8b4513';
          link.style.background = '#f5f0eb';
        }
      });
    }

    window.addEventListener('scroll', highlightNav);
    highlightNav();
  </script>
</body>
</html>

```

我已经创建了一个全新的学术主页 `index_new.html`。让我来介绍一下这个新设计的特点：

## 🎨 设计特点

### 字体选择
- **标题字体**: Cormorant Garamond — 优雅的衬线字体，适合学术环境
- **正文字体**: Source Sans 3 — 现代清晰的无衬线字体，易于阅读

### 配色方案
- 温暖的米色背景 (`#faf9f7`) 取代纯白，减少视觉疲劳
- 深褐色强调色 (`#8b4513`) — 学术、沉稳、专业
- 微妙的渐变背景效果增加层次感

### 布局改进
1. **固定导航栏** — 滚动时保持可见，方便快速导航
2. **卡片式论文展示** — 每篇论文独立成卡，悬停有微妙动效
3. **清晰的信息层级** — 标题、作者、会议、代码链接分层展示
4. **响应式设计** — 适配手机和平板设备

### 交互效果
- 页面加载时的淡入动画
- 社交图标悬停变色效果
- 导航栏滚动高亮当前区块
- 平滑滚动导航

### 内容优化
- 所有原有内容完整保留
- 招聘信息突出显示
- News 用日期标签更清晰
- 论文列表带代码链接按钮

您可以在浏览器中打开 `index_new.html` 预览效果。如果满意，可以将其重命名为 `index.html` 替换原文件。需要我帮您做任何调整吗？

---

**User**

在电脑浏览器打开时，字体可以稍微大一些，layout稍微宽一些。把所有的样式代码放到另一个专门的文件，@@index_new.html  只留给用户编辑内容。 另外，这个网页要在手机端打开的时候也显示合理

---

**Cursor**

我来把样式分离到单独的CSS文件，并调整字体大小和布局宽度，同时优化移动端显示。

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #faf9f7;
  --color-text: #1a1a1a;
  --color-text-secondary: #4a4a4a;
  --color-accent: #8b4513;
  --color-accent-light: #c4956a;
  --color-border: #e0dcd4;
  --color-card-bg: #ffffff;
  --color-tag: #f5f0eb;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 20%, rgba(139, 69, 19, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(139, 69, 19, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(250, 249, 247, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #fff7ed, #fef3e2);
  border: 1px solid #f5d0a9;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

现在更新 `index_new.html`，移除内联样式，引用外部CSS文件：

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Haoli Bai (柏昊立)</title>
  
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Source+Sans+3:wght@300;400;500;600&display=swap" rel="stylesheet">
  
  <!-- Main Stylesheet -->
  <link rel="stylesheet" href="style/main.css">
</head>
<body>
  <div class="container">
    
    <!-- ============================================
         Header Section
         ============================================ -->
    <header>
      <div class="header-content">
        <img src="img/square_light.jpg" alt="Haoli Bai" class="profile-image">
        <div class="header-info">
          <h1>Haoli Bai (柏昊立)</h1>
          <p class="affiliation">Researcher, Huawei Hong Kong Research Center</p>
          <p class="location">Hong Kong SAR, China</p>
          <p class="contact-email"><strong>Email:</strong> haolibai [at] gmail.com</p>
          <div class="social-links">
            <a href="https://scholar.google.com/citations?user=pk7jX3gAAAAJ&hl=zh-CN" title="Google Scholar">
              <img src="img/google_scholar.png" alt="Google Scholar">
            </a>
            <a href="https://dblp.org/pid/195/9712.html" title="DBLP">
              <img src="img/dblp.png" alt="DBLP">
            </a>
            <a href="https://github.com/haolibai" title="GitHub">
              <img src="img/github_s.jpg" alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/baihaoli-407136142/" title="LinkedIn">
              <img src="img/LinkedIn_s.png" alt="LinkedIn">
            </a>
          </div>
        </div>
      </div>
    </header>

    <!-- ============================================
         Navigation
         ============================================ -->
    <nav>
      <div class="container">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#publications">Publications</a></li>
          <li><a href="#talks">Talks</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#awards">Awards</a></li>
          <li><a href="#experience">Experience</a></li>
        </ul>
      </div>
    </nav>

    <!-- ============================================
         Main Content
         ============================================ -->
    <main>
      
      <!-- About Section -->
      <section id="about">
        <h2>About</h2>
        <div class="bio">
          <p>I am currently a researcher at the Language Model Lab, Huawei Hong Kong Research Center. I obtained my Ph.D. degree from The Chinese University of Hong Kong supervised by <a href="https://www.cse.cuhk.edu.hk/lyu/">Prof. Michael R. Lyu</a> and <a href="https://www.cse.cuhk.edu.hk/irwin.king/">Prof. Irwin King</a>, and the B.Eng. Degree from Yingcai Honors College of University of Electronic Science and Technology.</p>
          <p>Our team's effort is on large language models with topics spanning from pre-training, post-training, to agentic AI (e.g., deep research and coding agent). I am also an experienced researcher in LLM efficiency, e.g., compression and acceleration of LLMs.</p>
          <div class="hiring-notice">
            <span class="fire">🔥</span>
            <span><strong>[Hiring]</strong> We are constantly looking for full-time researchers and research interns with solid algorithm or system background (Base: HK or Shenzhen). Please connect by E-Mail.</span>
          </div>
        </div>
      </section>

      <!-- News Section -->
      <section id="news">
        <h2>News</h2>
        <ul class="news-list">
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">We will present the tutorial "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">Tutorial website</a></span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">I will give a talk on "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG 2025</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-9</span>
            <span class="news-content">Our paper <a href="https://arxiv.org/abs/2505.24680">"A Simple Linear Patch Revives Layer-Pruned Large Language Models"</a> is accepted by NeurIPS 2025.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-7</span>
            <span class="news-content">🔥 Our paper <a href="https://arxiv.org/abs/2504.04823v1">"Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models"</a> is accepted by COLM 2025. It was on the top-10 trending list on <a href="https://www.alphaxiv.org/abs/2504.04823">alphaXiv</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-4</span>
            <span class="news-content">I will serve as the Area Chair for NeurIPS 2025.</span>
          </li>
        </ul>
      </section>

      <!-- Publications Section -->
      <section id="publications">
        <h2>Selected Publications</h2>
        <p class="pub-note">*: Equal contribution; #: Corresponding author; +: Project lead</p>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2505.24680">A Simple Linear Patch Revives Layer-Pruned Large Language Models</a>
          </div>
          <div class="pub-authors">Xinrui Chen, <strong>Haoli Bai</strong><sup>#+</sup>, Tao Yuan, Ruikang Liu, Kang Zhao, Xianzhi Yu, Lu Hou, Tian Guan, Yonghong He, Chun Yuan<sup>#</sup></div>
          <div class="pub-venue">Proceedings of the 39th conference on Neural Information Processing Systems (NeurIPS), 2025.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2504.04823v1">Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models</a>
          </div>
          <div class="pub-authors">Ruikang Liu<sup>*</sup>, Yuxuan Sun<sup>*</sup>, Manyi Zhang<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Xianzhi Yu, Tiezheng Yu, Chun Yuan, Lu Hou<sup>#</sup></div>
          <div class="pub-venue">Conference on Language Modeling (COLM), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/Quantized-Reasoning-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2410.09426">FlatQuant: Flatness Matters for LLM Quantization</a>
          </div>
          <div class="pub-authors">Yuxuan Sun<sup>*</sup>, Ruikang Liu<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Han Bao, Kang Zhao, Yuening Li, Jiaxin Hu, Xianzhi Yu, Lu Hou, Chun Yuan, Xin Jiang, Wulong Liu, Jun Yao</div>
          <div class="pub-venue">International Conference on Machine Learning (ICML), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/FlatQuant">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://aclanthology.org/2024.naacl-long.264.pdf">Visually Guided Generative Text-Layout Pre-training for Document Intelligence</a>
          </div>
          <div class="pub-authors">Zhiming Mao, <strong>Haoli Bai</strong><sup>#+</sup>, Lu Hou, Lifeng Shang, Xin Jiang, Qun Liu, Kam-Fai Wong</div>
          <div class="pub-venue">The North American Chapter of the Association for Computational Linguistics (NAACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/Veason-silverbullet/ViTLP">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.01241">IntactKV: Improving Large Language Model Quantization by Keeping Pivot Tokens Intact</a>
          </div>
          <div class="pub-authors">Ruikang Liu, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Yuening Li, Han Gao, Zhengzhuo Xu, Lu Hou, Jun Yao, Chun Yuan</div>
          <div class="pub-venue">Findings of Annual Meeting of the Association for Computational Linguistics (ACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/IntactKV">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.07839v1">MoPE-CLIP: Structured Pruning for Efficient Vision-Language Models with Module-wise Pruning Error Metric</a>
          </div>
          <div class="pub-authors">Haokun Lin, <strong>Haoli Bai</strong><sup>+</sup>, Zhili Liu, Lu Hou, Muyi Sun, Linqi Song, Ying Wei, Zhenan Sun</div>
          <div class="pub-venue">Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2024.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://openreview.net/forum?id=Tr0lPx9woF">Plug-and-Play: An Efficient Post-training Pruning Method for Large Language Models</a>
          </div>
          <div class="pub-authors">Yingtao Zhang, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Jialin Zhao, Lu Hou, Carlo Vittorio Cannistraci</div>
          <div class="pub-venue">The Twelfth International Conference on Learning Representations (ICLR), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/biomedical-cybernetics/Relative-importance-and-activation-pruning">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2212.09621">Wukong-Reader: Multi-modal Pre-training for Fine-grained Visual Document Understanding</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Zhiguang Liu<sup>*</sup>, Xiaojun Meng<sup>*</sup>, Wentao Li, Shuang Liu, Nian Xie, Rongfu Zheng, Liangwei Wang, Lu Hou, Jiansheng Wei, Xin Jiang, Qun Liu</div>
          <div class="pub-venue">The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <span>Structured Pruning for Efficient Generative Pre-trained Language Models</span>
          </div>
          <div class="pub-authors">Chaofan Tao, Lu Hou<sup>+</sup>, <strong>Haoli Bai</strong><sup>+</sup>, Jiansheng Wei, Xin Jiang, Qun Liu, Ping Luo, Ngai Wong</div>
          <div class="pub-venue">Findings of The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2109.15082.pdf">Towards Efficient Post-training Quantization of Pre-trained Language Models</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Lu Hou, Lifeng Shang, Xin Jiang, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 36th conference on Neural Information Processing Systems (NeurIPS), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2111.09499">Dynamically pruning segformer for efficient semantic segmentation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Hongda Mao, Dinesh Nair</div>
          <div class="pub-venue">IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2012.15701">BinaryBERT: Pushing the Limit of BERT Quantization</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Wei Zhang, Lu Hou, Lifeng Shang, Jing Jin, Xin Jiang, Qun Liu, Michael Lyu, Irwin King</div>
          <div class="pub-venue">The 59th Annual Meeting of the Association for Computational Linguistics (ACL), 2021. <strong>Accepted with scores 5, 5, 4.</strong></div>
          <div class="pub-links">
            <a href="https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/BinaryBERT">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://proceedings.neurips.cc/paper/2020/file/42cd63cb189c30ed03e42ce2c069566c-Paper.pdf">Revisiting Parameter Sharing for Automatic Neural Channel Number Search</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Jiaxing Wang<sup>*</sup>, Jiaxiang Wu, Xupeng Shi, Junzhou Huang, Irwin King, Michael Lyu, Jian Cheng</div>
          <div class="pub-venue">Proceedings of the 34th conference on Neural Information Processing Systems (NeurIPS), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/APS-channel-search">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/1911.09450">Few Shot Network Compression via Cross Distillation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Jiaxiang Wu, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 34th AAAI Conference on Artificial Intelligence (AAAI), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/Cross-Distillation">Code</a>
            <a href="assets/aaai20_poster.pdf">Poster</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://17a11ed1-a-62cb3a1a-s-sites.googlegroups.com/site/nipsts2017/NIPS_2017_TSW_paper_19.pdf">Neural Relational Topic Models for Scientific Article Analysis</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zhuangbin Chen, Michael Lyu, Irwin King, Zenglin Xu</div>
          <div class="pub-venue">Proceedings of The 27th International Conference on Information and Knowledge Management (CIKM), 2018.</div>
          <div class="pub-links">
            <a href="https://github.com/zbchern/Neural-Relational-Topic-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="http://proceedings.mlr.press/v63/bai103.html">Hierarchical Probabilistic Matrix Factorization with Network Topology for Multi-relational Social Network</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zenglin Xu, Bin Liu, Yingming Li</div>
          <div class="pub-venue">Proceedings of The 8th Asian Conference on Machine Learning (ACML), 2016. <strong>Best Student Paper Runner-up</strong>.</div>
        </div>
      </section>

      <!-- Talks Section -->
      <section id="talks">
        <h2>Invited Talks</h2>
        <ul class="talks-list">
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="https://www.slai.edu.cn/">SLAI</a>, 2025. <a href="assets/quantization-pruning-public.pdf">[Slide]</a>
          </li>
          <li class="talk-item">
            "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP Tutorial, 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">[Tutorial website]</a>
          </li>
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG</a>, 2025.
          </li>
        </ul>
      </section>

      <!-- Projects Section -->
      <section id="projects">
        <h2>Projects</h2>
        <div class="project">
          <div class="project-header">
            <span class="project-title">PocketFlow: An Automated Framework for Compressing and Accelerating DNNs</span>
            <div class="project-links">
              <a href="https://github.com/tencent/PocketFlow">Code</a>
              <a href="https://pocketflow.github.io/">Doc</a>
            </div>
          </div>
          <p class="project-desc">PocketFlow automatically searches for optimal model compression strategies such as network pruning, quantization, knowledge distillation with little human efforts, and also supports TFLite deployment on Android devices. It has collected 2600+ stars and 480+ forks.</p>
        </div>
      </section>

      <!-- Services Section -->
      <section id="services">
        <h2>Services</h2>
        <div class="service-category">
          <div class="service-title">Area Chair</div>
          <div class="service-content">NeurIPS 2025</div>
        </div>
        <div class="service-category">
          <div class="service-title">Senior PC Member</div>
          <div class="service-content">IJCAI 2021</div>
        </div>
        <div class="service-category">
          <div class="service-title">PC Member</div>
          <div class="service-content">ICLR 22-25, ICML 21-25, NeurIPS 20-24, ACL ARR 25, COLM 25, ICCV 25, AAAI 19-21, IJCAI 20</div>
        </div>
        <div class="service-category">
          <div class="service-title">Journal Reviewer</div>
          <div class="service-content">T-PAMI, Neural Networks, etc.</div>
        </div>
      </section>

      <!-- Awards Section -->
      <section id="awards">
        <h2>Selected Awards</h2>
        <div class="timeline-item">
          <span class="timeline-title">Excellent Intern, Huawei Noah's Ark Lab</span>
          <span class="timeline-year">2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">AAAI Student Travel Grant</span>
          <span class="timeline-year">2020</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">ACM Student Travel Grant, CIKM</span>
          <span class="timeline-year">2018</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CUHK Postgraduate Student Scholarship</span>
          <span class="timeline-year">2017-2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Best Student Paper Runner-up, ACML</span>
          <span class="timeline-year">2016</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">National Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Tang Lixin Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
      </section>

      <!-- Experience Section -->
      <section id="experience">
        <h2>Experience</h2>
        
        <h3>Work Experience</h3>
        <div class="timeline-item">
          <span class="timeline-title">Applied Scientist Intern at <a href="https://www.amazon.jobs/en/business_categories/amazon-devices">Amazon Devices</a></span>
          <span class="timeline-year">2021 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="http://www.noahlab.com.hk/#/home">Huawei Noah's Ark Lab</a></span>
          <span class="timeline-year">2020 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="https://ai.tencent.com/ailab/index.html">Tencent AI Lab</a></span>
          <span class="timeline-year">2018 Summer</span>
        </div>

        <h3>Teaching Assistant</h3>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2020 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2019 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI1540: Introduction to C++</span>
          <span class="timeline-year">2018 Fall</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2018 Spring</span>
        </div>
      </section>

    </main>

    <!-- ============================================
         Footer
         ============================================ -->
    <footer>
      <div class="footer-content">
        <p>&copy; <span id="year"></span> Haoli Bai · <a href="#" id="top-link">Back to top ↑</a></p>
      </div>
      <div class="visitor-map">
        <script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=nQLu84viePq1dfXIYnjoGiQxqm-r7hYJeX8f_Oug7fo&cl=ffffff&w=a"></script>
      </div>
    </footer>

  </div>

  <!-- ============================================
       JavaScript
       ============================================ -->
  <script>
    // Set current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for navigation
    document.querySelectorAll('nav a, #top-link').forEach(link => {
      link.addEventListener('click', function(e) {
        if (this.id === 'top-link') {
          e.preventDefault();
          window.scrollTo({ top: 0, behavior: 'smooth' });
          return;
        }
        const href = this.getAttribute('href');
        if (href.startsWith('#')) {
          e.preventDefault();
          const target = document.querySelector(href);
          if (target) {
            target.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        }
      });
    });

    // Add scroll-based nav highlight
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('nav a');

    function highlightNav() {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 100;
        if (pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });

      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === `#${current}`) {
          link.classList.add('active');
        }
      });
    }

    window.addEventListener('scroll', highlightNav);
    highlightNav();
  </script>
</body>
</html>

```

已完成！现在文件结构更加清晰：

## 📁 文件结构

```
haolibai.github.io/
├── index_new.html      ← 只包含内容，方便编辑
├── style/
│   ├── main.css        ← 所有样式代码（新建）
│   └── jemdoc.css      ← 旧样式
└── img/
    └── ...
```

## ✨ 改进内容

### 1. 桌面端调整
| 项目 | 之前 | 现在 |
|------|------|------|
| 基础字体 | 16px | 17px |
| 大屏字体 (1200px+) | - | 18px |
| 布局宽度 | 860px | 960px |
| 大屏宽度 (1200px+) | - | 1000px |
| 头像尺寸 | 180px | 200px / 220px(大屏) |
| 标题字号 | 2.5rem | 2.75rem / 3rem(大屏) |

### 2. 响应式断点
- **大桌面** (1200px+): 更宽布局、更大字体
- **普通桌面** (1024-1199px): 标准布局
- **平板** (768-1023px): 中等布局，720px 内容宽度
- **手机** (≤767px): 单栏布局，头像居中，竖排时间线
- **小屏手机** (≤374px): 进一步缩小尺寸

### 3. HTML 文件简化
`index_new.html` 现在只有 **~320 行**（之前 980 行），结构清晰：
- 有注释标注每个区块
- 只需修改文字内容
- 样式完全分离到 CSS

您可以在浏览器中打开 `index_new.html` 预览效果，在电脑和手机上分别查看显示效果。如需进一步调整，请告诉我！

```plaintext
haolibai.github.io/
├── index_new.html      ← 只包含内容，方便编辑
├── style/
│   ├── main.css        ← 所有样式代码（新建）
│   └── jemdoc.css      ← 旧样式
└── img/
    └── ...
```

---

**User**

把@index.html里最后那个插件加到最后 @index.html:619-624 ；另外，我想尝试一下浅蓝色风格，显得更沉稳清新一些

---

**Cursor**

好的，我来添加访客地图插件并将风格改为浅蓝色。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Haoli Bai (柏昊立)</title>
  
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Source+Sans+3:wght@300;400;500;600&display=swap" rel="stylesheet">
  
  <!-- Main Stylesheet -->
  <link rel="stylesheet" href="style/main.css">
</head>
<body>
  <div class="container">
    
    <!-- ============================================
         Header Section
         ============================================ -->
    <header>
      <div class="header-content">
        <img src="img/square_light.jpg" alt="Haoli Bai" class="profile-image">
        <div class="header-info">
          <h1>Haoli Bai (柏昊立)</h1>
          <p class="affiliation">Researcher, Huawei Hong Kong Research Center</p>
          <p class="location">Hong Kong SAR, China</p>
          <p class="contact-email"><strong>Email:</strong> haolibai [at] gmail.com</p>
          <div class="social-links">
            <a href="https://scholar.google.com/citations?user=pk7jX3gAAAAJ&hl=zh-CN" title="Google Scholar">
              <img src="img/google_scholar.png" alt="Google Scholar">
            </a>
            <a href="https://dblp.org/pid/195/9712.html" title="DBLP">
              <img src="img/dblp.png" alt="DBLP">
            </a>
            <a href="https://github.com/haolibai" title="GitHub">
              <img src="img/github_s.jpg" alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/baihaoli-407136142/" title="LinkedIn">
              <img src="img/LinkedIn_s.png" alt="LinkedIn">
            </a>
          </div>
        </div>
      </div>
    </header>

    <!-- ============================================
         Navigation
         ============================================ -->
    <nav>
      <div class="container">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#publications">Publications</a></li>
          <li><a href="#talks">Talks</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#awards">Awards</a></li>
          <li><a href="#experience">Experience</a></li>
        </ul>
      </div>
    </nav>

    <!-- ============================================
         Main Content
         ============================================ -->
    <main>
      
      <!-- About Section -->
      <section id="about">
        <h2>About</h2>
        <div class="bio">
          <p>I am currently a researcher at the Language Model Lab, Huawei Hong Kong Research Center. I obtained my Ph.D. degree from The Chinese University of Hong Kong supervised by <a href="https://www.cse.cuhk.edu.hk/lyu/">Prof. Michael R. Lyu</a> and <a href="https://www.cse.cuhk.edu.hk/irwin.king/">Prof. Irwin King</a>, and the B.Eng. Degree from Yingcai Honors College of University of Electronic Science and Technology.</p>
          <p>Our team's effort is on large language models with topics spanning from pre-training, post-training, to agentic AI (e.g., deep research and coding agent). I am also an experienced researcher in LLM efficiency, e.g., compression and acceleration of LLMs.</p>
          <div class="hiring-notice">
            <span class="fire">🔥</span>
            <span><strong>[Hiring]</strong> We are constantly looking for full-time researchers and research interns with solid algorithm or system background (Base: HK or Shenzhen). Please connect by E-Mail.</span>
          </div>
        </div>
      </section>

      <!-- News Section -->
      <section id="news">
        <h2>News</h2>
        <ul class="news-list">
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">We will present the tutorial "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">Tutorial website</a></span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">I will give a talk on "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG 2025</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-9</span>
            <span class="news-content">Our paper <a href="https://arxiv.org/abs/2505.24680">"A Simple Linear Patch Revives Layer-Pruned Large Language Models"</a> is accepted by NeurIPS 2025.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-7</span>
            <span class="news-content">🔥 Our paper <a href="https://arxiv.org/abs/2504.04823v1">"Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models"</a> is accepted by COLM 2025. It was on the top-10 trending list on <a href="https://www.alphaxiv.org/abs/2504.04823">alphaXiv</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-4</span>
            <span class="news-content">I will serve as the Area Chair for NeurIPS 2025.</span>
          </li>
        </ul>
      </section>

      <!-- Publications Section -->
      <section id="publications">
        <h2>Selected Publications</h2>
        <p class="pub-note">*: Equal contribution; #: Corresponding author; +: Project lead</p>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2505.24680">A Simple Linear Patch Revives Layer-Pruned Large Language Models</a>
          </div>
          <div class="pub-authors">Xinrui Chen, <strong>Haoli Bai</strong><sup>#+</sup>, Tao Yuan, Ruikang Liu, Kang Zhao, Xianzhi Yu, Lu Hou, Tian Guan, Yonghong He, Chun Yuan<sup>#</sup></div>
          <div class="pub-venue">Proceedings of the 39th conference on Neural Information Processing Systems (NeurIPS), 2025.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2504.04823v1">Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models</a>
          </div>
          <div class="pub-authors">Ruikang Liu<sup>*</sup>, Yuxuan Sun<sup>*</sup>, Manyi Zhang<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Xianzhi Yu, Tiezheng Yu, Chun Yuan, Lu Hou<sup>#</sup></div>
          <div class="pub-venue">Conference on Language Modeling (COLM), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/Quantized-Reasoning-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2410.09426">FlatQuant: Flatness Matters for LLM Quantization</a>
          </div>
          <div class="pub-authors">Yuxuan Sun<sup>*</sup>, Ruikang Liu<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Han Bao, Kang Zhao, Yuening Li, Jiaxin Hu, Xianzhi Yu, Lu Hou, Chun Yuan, Xin Jiang, Wulong Liu, Jun Yao</div>
          <div class="pub-venue">International Conference on Machine Learning (ICML), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/FlatQuant">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://aclanthology.org/2024.naacl-long.264.pdf">Visually Guided Generative Text-Layout Pre-training for Document Intelligence</a>
          </div>
          <div class="pub-authors">Zhiming Mao, <strong>Haoli Bai</strong><sup>#+</sup>, Lu Hou, Lifeng Shang, Xin Jiang, Qun Liu, Kam-Fai Wong</div>
          <div class="pub-venue">The North American Chapter of the Association for Computational Linguistics (NAACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/Veason-silverbullet/ViTLP">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.01241">IntactKV: Improving Large Language Model Quantization by Keeping Pivot Tokens Intact</a>
          </div>
          <div class="pub-authors">Ruikang Liu, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Yuening Li, Han Gao, Zhengzhuo Xu, Lu Hou, Jun Yao, Chun Yuan</div>
          <div class="pub-venue">Findings of Annual Meeting of the Association for Computational Linguistics (ACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/IntactKV">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.07839v1">MoPE-CLIP: Structured Pruning for Efficient Vision-Language Models with Module-wise Pruning Error Metric</a>
          </div>
          <div class="pub-authors">Haokun Lin, <strong>Haoli Bai</strong><sup>+</sup>, Zhili Liu, Lu Hou, Muyi Sun, Linqi Song, Ying Wei, Zhenan Sun</div>
          <div class="pub-venue">Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2024.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://openreview.net/forum?id=Tr0lPx9woF">Plug-and-Play: An Efficient Post-training Pruning Method for Large Language Models</a>
          </div>
          <div class="pub-authors">Yingtao Zhang, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Jialin Zhao, Lu Hou, Carlo Vittorio Cannistraci</div>
          <div class="pub-venue">The Twelfth International Conference on Learning Representations (ICLR), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/biomedical-cybernetics/Relative-importance-and-activation-pruning">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2212.09621">Wukong-Reader: Multi-modal Pre-training for Fine-grained Visual Document Understanding</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Zhiguang Liu<sup>*</sup>, Xiaojun Meng<sup>*</sup>, Wentao Li, Shuang Liu, Nian Xie, Rongfu Zheng, Liangwei Wang, Lu Hou, Jiansheng Wei, Xin Jiang, Qun Liu</div>
          <div class="pub-venue">The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <span>Structured Pruning for Efficient Generative Pre-trained Language Models</span>
          </div>
          <div class="pub-authors">Chaofan Tao, Lu Hou<sup>+</sup>, <strong>Haoli Bai</strong><sup>+</sup>, Jiansheng Wei, Xin Jiang, Qun Liu, Ping Luo, Ngai Wong</div>
          <div class="pub-venue">Findings of The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2109.15082.pdf">Towards Efficient Post-training Quantization of Pre-trained Language Models</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Lu Hou, Lifeng Shang, Xin Jiang, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 36th conference on Neural Information Processing Systems (NeurIPS), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2111.09499">Dynamically pruning segformer for efficient semantic segmentation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Hongda Mao, Dinesh Nair</div>
          <div class="pub-venue">IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2012.15701">BinaryBERT: Pushing the Limit of BERT Quantization</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Wei Zhang, Lu Hou, Lifeng Shang, Jing Jin, Xin Jiang, Qun Liu, Michael Lyu, Irwin King</div>
          <div class="pub-venue">The 59th Annual Meeting of the Association for Computational Linguistics (ACL), 2021. <strong>Accepted with scores 5, 5, 4.</strong></div>
          <div class="pub-links">
            <a href="https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/BinaryBERT">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://proceedings.neurips.cc/paper/2020/file/42cd63cb189c30ed03e42ce2c069566c-Paper.pdf">Revisiting Parameter Sharing for Automatic Neural Channel Number Search</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Jiaxing Wang<sup>*</sup>, Jiaxiang Wu, Xupeng Shi, Junzhou Huang, Irwin King, Michael Lyu, Jian Cheng</div>
          <div class="pub-venue">Proceedings of the 34th conference on Neural Information Processing Systems (NeurIPS), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/APS-channel-search">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/1911.09450">Few Shot Network Compression via Cross Distillation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Jiaxiang Wu, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 34th AAAI Conference on Artificial Intelligence (AAAI), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/Cross-Distillation">Code</a>
            <a href="assets/aaai20_poster.pdf">Poster</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://17a11ed1-a-62cb3a1a-s-sites.googlegroups.com/site/nipsts2017/NIPS_2017_TSW_paper_19.pdf">Neural Relational Topic Models for Scientific Article Analysis</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zhuangbin Chen, Michael Lyu, Irwin King, Zenglin Xu</div>
          <div class="pub-venue">Proceedings of The 27th International Conference on Information and Knowledge Management (CIKM), 2018.</div>
          <div class="pub-links">
            <a href="https://github.com/zbchern/Neural-Relational-Topic-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="http://proceedings.mlr.press/v63/bai103.html">Hierarchical Probabilistic Matrix Factorization with Network Topology for Multi-relational Social Network</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zenglin Xu, Bin Liu, Yingming Li</div>
          <div class="pub-venue">Proceedings of The 8th Asian Conference on Machine Learning (ACML), 2016. <strong>Best Student Paper Runner-up</strong>.</div>
        </div>
      </section>

      <!-- Talks Section -->
      <section id="talks">
        <h2>Invited Talks</h2>
        <ul class="talks-list">
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="https://www.slai.edu.cn/">SLAI</a>, 2025. <a href="assets/quantization-pruning-public.pdf">[Slide]</a>
          </li>
          <li class="talk-item">
            "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP Tutorial, 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">[Tutorial website]</a>
          </li>
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG</a>, 2025.
          </li>
        </ul>
      </section>

      <!-- Projects Section -->
      <section id="projects">
        <h2>Projects</h2>
        <div class="project">
          <div class="project-header">
            <span class="project-title">PocketFlow: An Automated Framework for Compressing and Accelerating DNNs</span>
            <div class="project-links">
              <a href="https://github.com/tencent/PocketFlow">Code</a>
              <a href="https://pocketflow.github.io/">Doc</a>
            </div>
          </div>
          <p class="project-desc">PocketFlow automatically searches for optimal model compression strategies such as network pruning, quantization, knowledge distillation with little human efforts, and also supports TFLite deployment on Android devices. It has collected 2600+ stars and 480+ forks.</p>
        </div>
      </section>

      <!-- Services Section -->
      <section id="services">
        <h2>Services</h2>
        <div class="service-category">
          <div class="service-title">Area Chair</div>
          <div class="service-content">NeurIPS 2025</div>
        </div>
        <div class="service-category">
          <div class="service-title">Senior PC Member</div>
          <div class="service-content">IJCAI 2021</div>
        </div>
        <div class="service-category">
          <div class="service-title">PC Member</div>
          <div class="service-content">ICLR 22-25, ICML 21-25, NeurIPS 20-24, ACL ARR 25, COLM 25, ICCV 25, AAAI 19-21, IJCAI 20</div>
        </div>
        <div class="service-category">
          <div class="service-title">Journal Reviewer</div>
          <div class="service-content">T-PAMI, Neural Networks, etc.</div>
        </div>
      </section>

      <!-- Awards Section -->
      <section id="awards">
        <h2>Selected Awards</h2>
        <div class="timeline-item">
          <span class="timeline-title">Excellent Intern, Huawei Noah's Ark Lab</span>
          <span class="timeline-year">2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">AAAI Student Travel Grant</span>
          <span class="timeline-year">2020</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">ACM Student Travel Grant, CIKM</span>
          <span class="timeline-year">2018</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CUHK Postgraduate Student Scholarship</span>
          <span class="timeline-year">2017-2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Best Student Paper Runner-up, ACML</span>
          <span class="timeline-year">2016</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">National Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Tang Lixin Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
      </section>

      <!-- Experience Section -->
      <section id="experience">
        <h2>Experience</h2>
        
        <h3>Work Experience</h3>
        <div class="timeline-item">
          <span class="timeline-title">Applied Scientist Intern at <a href="https://www.amazon.jobs/en/business_categories/amazon-devices">Amazon Devices</a></span>
          <span class="timeline-year">2021 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="http://www.noahlab.com.hk/#/home">Huawei Noah's Ark Lab</a></span>
          <span class="timeline-year">2020 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="https://ai.tencent.com/ailab/index.html">Tencent AI Lab</a></span>
          <span class="timeline-year">2018 Summer</span>
        </div>

        <h3>Teaching Assistant</h3>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2020 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2019 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI1540: Introduction to C++</span>
          <span class="timeline-year">2018 Fall</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2018 Spring</span>
        </div>
      </section>

    </main>

    <!-- ============================================
         Footer
         ============================================ -->
    <footer>
      <div class="footer-content">
        <p>&copy; <span id="year"></span> Haoli Bai · <a href="#" id="top-link">Back to top ↑</a></p>
      </div>
      <div class="visitor-map">
        <div id="clustrmaps-widget">
          <script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=nQLu84viePq1dfXIYnjoGiQxqm-r7hYJeX8f_Oug7fo&cl=ffffff&w=a"></script>
        </div>
      </div>
    </footer>

  </div>

  <!-- ============================================
       JavaScript
       ============================================ -->
  <script>
    // Set current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for navigation
    document.querySelectorAll('nav a, #top-link').forEach(link => {
      link.addEventListener('click', function(e) {
        if (this.id === 'top-link') {
          e.preventDefault();
          window.scrollTo({ top: 0, behavior: 'smooth' });
          return;
        }
        const href = this.getAttribute('href');
        if (href.startsWith('#')) {
          e.preventDefault();
          const target = document.querySelector(href);
          if (target) {
            target.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        }
      });
    });

    // Add scroll-based nav highlight
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('nav a');

    function highlightNav() {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 100;
        if (pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });

      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === `#${current}`) {
          link.classList.add('active');
        }
      });
    }

    window.addEventListener('scroll', highlightNav);
    highlightNav();
  </script>
</body>
</html>

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 20%, rgba(139, 69, 19, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(139, 69, 19, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(250, 249, 247, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #fff7ed, #fef3e2);
  border: 1px solid #f5d0a9;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(250, 249, 247, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #fff7ed, #fef3e2);
  border: 1px solid #f5d0a9;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(250, 249, 247, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(250, 249, 247, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Cormorant Garamond', Georgia, serif;
  --font-sans: 'Source Sans 3', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

完成！已添加访客地图插件并切换到浅蓝色风格。

## 🎨 浅蓝色配色方案

| 元素 | 颜色 | 效果 |
|------|------|------|
| 背景 | `#f7f9fc` | 带蓝调的浅灰白 |
| 主文字 | `#1a2332` | 深藏青色 |
| 次文字 | `#4a5568` | 灰蓝色 |
| 强调色 | `#2563a8` | 沉稳深蓝 |
| 浅强调 | `#60a5c8` | 清新天蓝 |
| 边框 | `#d8e3ed` | 淡蓝灰 |
| 标签 | `#e8f1f8` | 浅蓝底色 |

## ✅ 更新内容

1. **访客地图插件** - 已添加到页面底部
2. **整体配色** - 切换为浅蓝色系
3. **背景渐变** - 更新为蓝色调的微妙渐变
4. **招聘通知** - 改为蓝色渐变背景
5. **导航栏** - 背景透明度与新配色协调

新风格更加**沉稳、清新、专业**，非常适合学术主页。您可以刷新浏览器查看效果！如需调整色调深浅，随时告诉我。

---

**User**

不错。我想换一个字体，稍微粗一些的，能够显得更显眼一些。字体也能稍微大一号

---

**Cursor**

好的，我来更换为更粗、更显眼的字体并增大字号。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Haoli Bai (柏昊立)</title>
  
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;1,9..40,400&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">
  
  <!-- Main Stylesheet -->
  <link rel="stylesheet" href="style/main.css">
</head>
<body>
  <div class="container">
    
    <!-- ============================================
         Header Section
         ============================================ -->
    <header>
      <div class="header-content">
        <img src="img/square_light.jpg" alt="Haoli Bai" class="profile-image">
        <div class="header-info">
          <h1>Haoli Bai (柏昊立)</h1>
          <p class="affiliation">Researcher, Huawei Hong Kong Research Center</p>
          <p class="location">Hong Kong SAR, China</p>
          <p class="contact-email"><strong>Email:</strong> haolibai [at] gmail.com</p>
          <div class="social-links">
            <a href="https://scholar.google.com/citations?user=pk7jX3gAAAAJ&hl=zh-CN" title="Google Scholar">
              <img src="img/google_scholar.png" alt="Google Scholar">
            </a>
            <a href="https://dblp.org/pid/195/9712.html" title="DBLP">
              <img src="img/dblp.png" alt="DBLP">
            </a>
            <a href="https://github.com/haolibai" title="GitHub">
              <img src="img/github_s.jpg" alt="GitHub">
            </a>
            <a href="https://www.linkedin.com/in/baihaoli-407136142/" title="LinkedIn">
              <img src="img/LinkedIn_s.png" alt="LinkedIn">
            </a>
          </div>
        </div>
      </div>
    </header>

    <!-- ============================================
         Navigation
         ============================================ -->
    <nav>
      <div class="container">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#news">News</a></li>
          <li><a href="#publications">Publications</a></li>
          <li><a href="#talks">Talks</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#awards">Awards</a></li>
          <li><a href="#experience">Experience</a></li>
        </ul>
      </div>
    </nav>

    <!-- ============================================
         Main Content
         ============================================ -->
    <main>
      
      <!-- About Section -->
      <section id="about">
        <h2>About</h2>
        <div class="bio">
          <p>I am currently a researcher at the Language Model Lab, Huawei Hong Kong Research Center. I obtained my Ph.D. degree from The Chinese University of Hong Kong supervised by <a href="https://www.cse.cuhk.edu.hk/lyu/">Prof. Michael R. Lyu</a> and <a href="https://www.cse.cuhk.edu.hk/irwin.king/">Prof. Irwin King</a>, and the B.Eng. Degree from Yingcai Honors College of University of Electronic Science and Technology.</p>
          <p>Our team's effort is on large language models with topics spanning from pre-training, post-training, to agentic AI (e.g., deep research and coding agent). I am also an experienced researcher in LLM efficiency, e.g., compression and acceleration of LLMs.</p>
          <div class="hiring-notice">
            <span class="fire">🔥</span>
            <span><strong>[Hiring]</strong> We are constantly looking for full-time researchers and research interns with solid algorithm or system background (Base: HK or Shenzhen). Please connect by E-Mail.</span>
          </div>
        </div>
      </section>

      <!-- News Section -->
      <section id="news">
        <h2>News</h2>
        <ul class="news-list">
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">We will present the tutorial "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">Tutorial website</a></span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-11</span>
            <span class="news-content">I will give a talk on "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG 2025</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-9</span>
            <span class="news-content">Our paper <a href="https://arxiv.org/abs/2505.24680">"A Simple Linear Patch Revives Layer-Pruned Large Language Models"</a> is accepted by NeurIPS 2025.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-7</span>
            <span class="news-content">🔥 Our paper <a href="https://arxiv.org/abs/2504.04823v1">"Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models"</a> is accepted by COLM 2025. It was on the top-10 trending list on <a href="https://www.alphaxiv.org/abs/2504.04823">alphaXiv</a>.</span>
          </li>
          <li class="news-item">
            <span class="news-date">2025-4</span>
            <span class="news-content">I will serve as the Area Chair for NeurIPS 2025.</span>
          </li>
        </ul>
      </section>

      <!-- Publications Section -->
      <section id="publications">
        <h2>Selected Publications</h2>
        <p class="pub-note">*: Equal contribution; #: Corresponding author; +: Project lead</p>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2505.24680">A Simple Linear Patch Revives Layer-Pruned Large Language Models</a>
          </div>
          <div class="pub-authors">Xinrui Chen, <strong>Haoli Bai</strong><sup>#+</sup>, Tao Yuan, Ruikang Liu, Kang Zhao, Xianzhi Yu, Lu Hou, Tian Guan, Yonghong He, Chun Yuan<sup>#</sup></div>
          <div class="pub-venue">Proceedings of the 39th conference on Neural Information Processing Systems (NeurIPS), 2025.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2504.04823v1">Quantization Hurts Reasoning? An Empirical Study on Quantized Reasoning Models</a>
          </div>
          <div class="pub-authors">Ruikang Liu<sup>*</sup>, Yuxuan Sun<sup>*</sup>, Manyi Zhang<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Xianzhi Yu, Tiezheng Yu, Chun Yuan, Lu Hou<sup>#</sup></div>
          <div class="pub-venue">Conference on Language Modeling (COLM), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/Quantized-Reasoning-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2410.09426">FlatQuant: Flatness Matters for LLM Quantization</a>
          </div>
          <div class="pub-authors">Yuxuan Sun<sup>*</sup>, Ruikang Liu<sup>*</sup>, <strong>Haoli Bai</strong><sup>#+</sup>, Han Bao, Kang Zhao, Yuening Li, Jiaxin Hu, Xianzhi Yu, Lu Hou, Chun Yuan, Xin Jiang, Wulong Liu, Jun Yao</div>
          <div class="pub-venue">International Conference on Machine Learning (ICML), 2025.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/FlatQuant">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://aclanthology.org/2024.naacl-long.264.pdf">Visually Guided Generative Text-Layout Pre-training for Document Intelligence</a>
          </div>
          <div class="pub-authors">Zhiming Mao, <strong>Haoli Bai</strong><sup>#+</sup>, Lu Hou, Lifeng Shang, Xin Jiang, Qun Liu, Kam-Fai Wong</div>
          <div class="pub-venue">The North American Chapter of the Association for Computational Linguistics (NAACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/Veason-silverbullet/ViTLP">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.01241">IntactKV: Improving Large Language Model Quantization by Keeping Pivot Tokens Intact</a>
          </div>
          <div class="pub-authors">Ruikang Liu, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Yuening Li, Han Gao, Zhengzhuo Xu, Lu Hou, Jun Yao, Chun Yuan</div>
          <div class="pub-venue">Findings of Annual Meeting of the Association for Computational Linguistics (ACL), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/ruikangliu/IntactKV">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2403.07839v1">MoPE-CLIP: Structured Pruning for Efficient Vision-Language Models with Module-wise Pruning Error Metric</a>
          </div>
          <div class="pub-authors">Haokun Lin, <strong>Haoli Bai</strong><sup>+</sup>, Zhili Liu, Lu Hou, Muyi Sun, Linqi Song, Ying Wei, Zhenan Sun</div>
          <div class="pub-venue">Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2024.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://openreview.net/forum?id=Tr0lPx9woF">Plug-and-Play: An Efficient Post-training Pruning Method for Large Language Models</a>
          </div>
          <div class="pub-authors">Yingtao Zhang, <strong>Haoli Bai</strong><sup>+</sup>, Haokun Lin, Jialin Zhao, Lu Hou, Carlo Vittorio Cannistraci</div>
          <div class="pub-venue">The Twelfth International Conference on Learning Representations (ICLR), 2024.</div>
          <div class="pub-links">
            <a href="https://github.com/biomedical-cybernetics/Relative-importance-and-activation-pruning">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2212.09621">Wukong-Reader: Multi-modal Pre-training for Fine-grained Visual Document Understanding</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Zhiguang Liu<sup>*</sup>, Xiaojun Meng<sup>*</sup>, Wentao Li, Shuang Liu, Nian Xie, Rongfu Zheng, Liangwei Wang, Lu Hou, Jiansheng Wei, Xin Jiang, Qun Liu</div>
          <div class="pub-venue">The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <span>Structured Pruning for Efficient Generative Pre-trained Language Models</span>
          </div>
          <div class="pub-authors">Chaofan Tao, Lu Hou<sup>+</sup>, <strong>Haoli Bai</strong><sup>+</sup>, Jiansheng Wei, Xin Jiang, Qun Liu, Ping Luo, Ngai Wong</div>
          <div class="pub-venue">Findings of The 61th Annual Meeting of the Association for Computational Linguistics (ACL), 2023.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/pdf/2109.15082.pdf">Towards Efficient Post-training Quantization of Pre-trained Language Models</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Lu Hou, Lifeng Shang, Xin Jiang, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 36th conference on Neural Information Processing Systems (NeurIPS), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2111.09499">Dynamically pruning segformer for efficient semantic segmentation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Hongda Mao, Dinesh Nair</div>
          <div class="pub-venue">IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2022.</div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/2012.15701">BinaryBERT: Pushing the Limit of BERT Quantization</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Wei Zhang, Lu Hou, Lifeng Shang, Jing Jin, Xin Jiang, Qun Liu, Michael Lyu, Irwin King</div>
          <div class="pub-venue">The 59th Annual Meeting of the Association for Computational Linguistics (ACL), 2021. <strong>Accepted with scores 5, 5, 4.</strong></div>
          <div class="pub-links">
            <a href="https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/BinaryBERT">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://proceedings.neurips.cc/paper/2020/file/42cd63cb189c30ed03e42ce2c069566c-Paper.pdf">Revisiting Parameter Sharing for Automatic Neural Channel Number Search</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong><sup>*</sup>, Jiaxing Wang<sup>*</sup>, Jiaxiang Wu, Xupeng Shi, Junzhou Huang, Irwin King, Michael Lyu, Jian Cheng</div>
          <div class="pub-venue">Proceedings of the 34th conference on Neural Information Processing Systems (NeurIPS), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/APS-channel-search">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://arxiv.org/abs/1911.09450">Few Shot Network Compression via Cross Distillation</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Jiaxiang Wu, Irwin King, Michael Lyu</div>
          <div class="pub-venue">Proceedings of the 34th AAAI Conference on Artificial Intelligence (AAAI), 2020.</div>
          <div class="pub-links">
            <a href="https://github.com/haolibai/Cross-Distillation">Code</a>
            <a href="assets/aaai20_poster.pdf">Poster</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="https://17a11ed1-a-62cb3a1a-s-sites.googlegroups.com/site/nipsts2017/NIPS_2017_TSW_paper_19.pdf">Neural Relational Topic Models for Scientific Article Analysis</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zhuangbin Chen, Michael Lyu, Irwin King, Zenglin Xu</div>
          <div class="pub-venue">Proceedings of The 27th International Conference on Information and Knowledge Management (CIKM), 2018.</div>
          <div class="pub-links">
            <a href="https://github.com/zbchern/Neural-Relational-Topic-Models">Code</a>
          </div>
        </div>

        <div class="publication">
          <div class="pub-title">
            <a href="http://proceedings.mlr.press/v63/bai103.html">Hierarchical Probabilistic Matrix Factorization with Network Topology for Multi-relational Social Network</a>
          </div>
          <div class="pub-authors"><strong>Haoli Bai</strong>, Zenglin Xu, Bin Liu, Yingming Li</div>
          <div class="pub-venue">Proceedings of The 8th Asian Conference on Machine Learning (ACML), 2016. <strong>Best Student Paper Runner-up</strong>.</div>
        </div>
      </section>

      <!-- Talks Section -->
      <section id="talks">
        <h2>Invited Talks</h2>
        <ul class="talks-list">
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="https://www.slai.edu.cn/">SLAI</a>, 2025. <a href="assets/quantization-pruning-public.pdf">[Slide]</a>
          </li>
          <li class="talk-item">
            "Efficient Inference for Large Language Models – Algorithm, Model, and System" at EMNLP Tutorial, 2025. <a href="https://haolibai.github.io/emnlp-2025-tutorial-efficiency/">[Tutorial website]</a>
          </li>
          <li class="talk-item">
            "Quantization and Pruning of Large Language Models: Challenges, Techniques and Opportunities" at <a href="http://lmg.cipsc.org.cn/conference/lmg2025/subForum/subForum4/index.html">LMG</a>, 2025.
          </li>
        </ul>
      </section>

      <!-- Projects Section -->
      <section id="projects">
        <h2>Projects</h2>
        <div class="project">
          <div class="project-header">
            <span class="project-title">PocketFlow: An Automated Framework for Compressing and Accelerating DNNs</span>
            <div class="project-links">
              <a href="https://github.com/tencent/PocketFlow">Code</a>
              <a href="https://pocketflow.github.io/">Doc</a>
            </div>
          </div>
          <p class="project-desc">PocketFlow automatically searches for optimal model compression strategies such as network pruning, quantization, knowledge distillation with little human efforts, and also supports TFLite deployment on Android devices. It has collected 2600+ stars and 480+ forks.</p>
        </div>
      </section>

      <!-- Services Section -->
      <section id="services">
        <h2>Services</h2>
        <div class="service-category">
          <div class="service-title">Area Chair</div>
          <div class="service-content">NeurIPS 2025</div>
        </div>
        <div class="service-category">
          <div class="service-title">Senior PC Member</div>
          <div class="service-content">IJCAI 2021</div>
        </div>
        <div class="service-category">
          <div class="service-title">PC Member</div>
          <div class="service-content">ICLR 22-25, ICML 21-25, NeurIPS 20-24, ACL ARR 25, COLM 25, ICCV 25, AAAI 19-21, IJCAI 20</div>
        </div>
        <div class="service-category">
          <div class="service-title">Journal Reviewer</div>
          <div class="service-content">T-PAMI, Neural Networks, etc.</div>
        </div>
      </section>

      <!-- Awards Section -->
      <section id="awards">
        <h2>Selected Awards</h2>
        <div class="timeline-item">
          <span class="timeline-title">Excellent Intern, Huawei Noah's Ark Lab</span>
          <span class="timeline-year">2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">AAAI Student Travel Grant</span>
          <span class="timeline-year">2020</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">ACM Student Travel Grant, CIKM</span>
          <span class="timeline-year">2018</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CUHK Postgraduate Student Scholarship</span>
          <span class="timeline-year">2017-2021</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Best Student Paper Runner-up, ACML</span>
          <span class="timeline-year">2016</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">National Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Tang Lixin Scholarship</span>
          <span class="timeline-year">2015</span>
        </div>
      </section>

      <!-- Experience Section -->
      <section id="experience">
        <h2>Experience</h2>
        
        <h3>Work Experience</h3>
        <div class="timeline-item">
          <span class="timeline-title">Applied Scientist Intern at <a href="https://www.amazon.jobs/en/business_categories/amazon-devices">Amazon Devices</a></span>
          <span class="timeline-year">2021 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="http://www.noahlab.com.hk/#/home">Huawei Noah's Ark Lab</a></span>
          <span class="timeline-year">2020 Summer</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">Research Intern at <a href="https://ai.tencent.com/ailab/index.html">Tencent AI Lab</a></span>
          <span class="timeline-year">2018 Summer</span>
        </div>

        <h3>Teaching Assistant</h3>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2020 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2019 Spring</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI1540: Introduction to C++</span>
          <span class="timeline-year">2018 Fall</span>
        </div>
        <div class="timeline-item">
          <span class="timeline-title">CSCI3100: Software Engineering</span>
          <span class="timeline-year">2018 Spring</span>
        </div>
      </section>

    </main>

    <!-- ============================================
         Footer
         ============================================ -->
    <footer>
      <div class="footer-content">
        <p>&copy; <span id="year"></span> Haoli Bai · <a href="#" id="top-link">Back to top ↑</a></p>
      </div>
      <div class="visitor-map">
        <div id="clustrmaps-widget">
          <script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=nQLu84viePq1dfXIYnjoGiQxqm-r7hYJeX8f_Oug7fo&cl=ffffff&w=a"></script>
        </div>
      </div>
    </footer>

  </div>

  <!-- ============================================
       JavaScript
       ============================================ -->
  <script>
    // Set current year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for navigation
    document.querySelectorAll('nav a, #top-link').forEach(link => {
      link.addEventListener('click', function(e) {
        if (this.id === 'top-link') {
          e.preventDefault();
          window.scrollTo({ top: 0, behavior: 'smooth' });
          return;
        }
        const href = this.getAttribute('href');
        if (href.startsWith('#')) {
          e.preventDefault();
          const target = document.querySelector(href);
          if (target) {
            target.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        }
      });
    });

    // Add scroll-based nav highlight
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('nav a');

    function highlightNav() {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 100;
        if (pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });

      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === `#${current}`) {
          link.classList.add('active');
        }
      });
    }

    window.addEventListener('scroll', highlightNav);
    highlightNav();
  </script>
</body>
</html>

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 17px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.75rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.15rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.6rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 18px;
  }
  
  .header-info h1 {
    font-size: 3rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.75rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.25rem;
  }
  
  .profile-image {
    width: 160px;
    height: 160px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 15px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 14px;
  }
  
  .header-info h1 {
    font-size: 1.6rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.8rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #1a2332;
  --color-text-secondary: #4a5568;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

完成！已更换为更粗、更显眼的字体并增大字号。

## 🔤 新字体

| 用途 | 之前 | 现在 |
|------|------|------|
| **正文** | Source Sans 3 (纤细) | **DM Sans** (几何风格，更粗壮) |
| **标题** | Cormorant Garamond | **Playfair Display** (优雅粗体衬线) |

## 📏 字号调整

| 屏幕 | 之前 | 现在 |
|------|------|------|
| 大桌面 (1200px+) | 18px | **19px** |
| 普通桌面 | 17px | **18px** |
| 平板 | 16px | **17px** |
| 手机 | 15px | **16px** |
| 小屏手机 | 14px | **15px** |

## ✨ 其他调整

- **姓名标题**: 字重 600 → **700**，字号更大
- **职位信息**: 加粗为 **500** 字重
- **区块标题 (h2)**: 字重 **700**，字号 1.75rem → 1.85rem (大屏)
- **论文标题**: 1.05rem → **1.1rem**
- **导航链接**: 0.95rem → **1rem**

新字体 **DM Sans** 笔画更粗，视觉更清晰；**Playfair Display** 标题字体优雅且醒目，非常适合学术主页。刷新浏览器即可看到效果！

---

**User**

不错，网页灰色的主要字体再稍微更黑一些，显得更加显眼

---

**Cursor**

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #141d2b;
  --color-text-secondary: #374151;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

完成！字体颜色更深了：

| 文字类型 | 之前 | 现在 |
|----------|------|------|
| 主文字 | `#1a2332` | `#141d2b` (更深) |
| 次文字 | `#4a5568` (浅灰) | `#374151` (深灰) |

次要文字颜色深了约 **20%**，现在阅读起来更加清晰醒目。刷新页面即可看到效果！

---

**User**

照片框背后可以做一个淡淡的阴影效果。主字体可以再黑一点，并大一号。About
News
Publications
Talks
Projects
Services
Awards
Experience 这些不要放到白框里

---

**Cursor**

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

/* Remove duplicate hover - already defined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  white-space: nowrap;
}

nav a:hover,
nav a.active {
  color: #1d4d7c;
  background: var(--color-tag);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

/* Remove duplicate hover - already defined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 19px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

/* Remove duplicate hover - already defined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 20px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

/* Remove duplicate hover - already defined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 20px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 18px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 16px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

.profile-image:hover {
  transform: translateY(-4px);
}

/* Remove duplicate hover - already defined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 20px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 18px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

让我清理一下重复的代码：

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

/* Profile image hover is combined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 20px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 18px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

```css
/* ============================================
   Academic Personal Website Stylesheet
   Author: Haoli Bai
   ============================================ */

/* ============================================
   CSS Variables
   ============================================ */
:root {
  --color-bg: #f7f9fc;
  --color-text: #0f1419;
  --color-text-secondary: #2d3748;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
  --spacing-unit: 1rem;
}

/* ============================================
   Reset & Base
   ============================================ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

/* Subtle background pattern */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

/* ============================================
   Layout
   ============================================ */
.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 calc(var(--spacing-unit) * 2);
}

/* ============================================
   Header
   ============================================ */
header {
  padding: calc(var(--spacing-unit) * 4) 0 calc(var(--spacing-unit) * 3);
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: calc(var(--spacing-unit) * 3);
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.08);
  flex-shrink: 0;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.12);
}

/* Profile image hover is combined above */

.header-info {
  flex: 1;
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

.contact-email strong {
  color: var(--color-text);
}

/* ============================================
   Social Links
   ============================================ */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s ease;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img {
  filter: brightness(0) invert(1);
}

.social-links img {
  width: 22px;
  height: 22px;
  transition: filter 0.2s ease;
}

/* ============================================
   Navigation
   ============================================ */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: calc(var(--spacing-unit) * 2);
}

nav ul {
  list-style: none;
  display: flex;
  gap: 0.25rem;
  padding: 0.75rem 0;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-radius: 0;
  transition: all 0.2s ease;
  white-space: nowrap;
  background: transparent;
  border-bottom: 2px solid transparent;
}

nav a:hover,
nav a.active {
  color: var(--color-accent);
  background: transparent;
  border-bottom: 2px solid var(--color-accent);
}

/* ============================================
   Sections
   ============================================ */
section {
  margin-bottom: calc(var(--spacing-unit) * 3.5);
  animation: fadeInUp 0.6s ease-out backwards;
}

section:nth-child(2) { animation-delay: 0.1s; }
section:nth-child(3) { animation-delay: 0.15s; }
section:nth-child(4) { animation-delay: 0.2s; }
section:nth-child(5) { animation-delay: 0.25s; }
section:nth-child(6) { animation-delay: 0.3s; }

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: calc(var(--spacing-unit) * 1.25);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 1.5rem 0 0.75rem;
}

/* ============================================
   Bio Section
   ============================================ */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.bio a:hover {
  border-bottom-color: var(--color-accent);
}

.bio p + p {
  margin-top: 1rem;
}

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

.hiring-notice .fire {
  font-size: 1.1rem;
}

/* ============================================
   News Section
   ============================================ */
.news-list {
  list-style: none;
}

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.news-content a:hover {
  text-decoration: underline;
}

/* ============================================
   Publications Section
   ============================================ */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s ease;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a {
  color: var(--color-text);
  text-decoration: none;
  transition: color 0.2s ease;
}

.pub-title a:hover {
  color: var(--color-accent);
}

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.pub-links a:hover {
  background: var(--color-accent);
  color: white;
}

/* ============================================
   Talks Section
   ============================================ */
.talks-list {
  list-style: none;
}

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-item a {
  color: var(--color-accent);
  text-decoration: none;
}

.talk-item a:hover {
  text-decoration: underline;
}

/* ============================================
   Projects Section
   ============================================ */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-shrink: 0;
}

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s ease;
}

.project-links a:hover {
  background: var(--color-accent);
  color: white;
}

.project-desc {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

/* ============================================
   Services Section
   ============================================ */
.service-category {
  margin-bottom: 1rem;
}

.service-title {
  font-weight: 600;
  color: var(--color-text);
  font-size: 1rem;
  margin-bottom: 0.25rem;
}

.service-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
}

/* ============================================
   Timeline (Awards & Experience)
   ============================================ */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child {
  border-bottom: none;
}

.timeline-title {
  color: var(--color-text);
}

.timeline-title a {
  color: var(--color-accent);
  text-decoration: none;
}

.timeline-title a:hover {
  text-decoration: underline;
}

.timeline-year {
  color: var(--color-text-secondary);
  flex-shrink: 0;
  margin-left: 1rem;
}

/* ============================================
   Footer
   ============================================ */
footer {
  margin-top: calc(var(--spacing-unit) * 4);
  padding: calc(var(--spacing-unit) * 2) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.footer-content a {
  color: var(--color-accent);
  text-decoration: none;
}

.footer-content a:hover {
  text-decoration: underline;
}

.visitor-map {
  max-width: 300px;
  margin: 0 auto;
}

/* ============================================
   Animations
   ============================================ */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   Large Desktop (1200px+)
   ============================================ */
@media (min-width: 1200px) {
  :root {
    --max-width: 1000px;
  }
  
  body {
    font-size: 20px;
  }
  
  .header-info h1 {
    font-size: 3.1rem;
  }
  
  .profile-image {
    width: 220px;
    height: 220px;
  }
  
  h2 {
    font-size: 1.85rem;
  }
}

/* ============================================
   Tablet (768px - 1023px)
   ============================================ */
@media (max-width: 1023px) {
  :root {
    --max-width: 720px;
  }
  
  body {
    font-size: 18px;
  }
  
  .container {
    padding: 0 calc(var(--spacing-unit) * 1.5);
  }
  
  .header-info h1 {
    font-size: 2.35rem;
  }
  
  .profile-image {
    width: 170px;
    height: 170px;
  }
}

/* ============================================
   Mobile (max-width: 767px)
   ============================================ */
@media (max-width: 767px) {
  body {
    font-size: 17px;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  header {
    padding: calc(var(--spacing-unit) * 2.5) 0 calc(var(--spacing-unit) * 2);
  }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: calc(var(--spacing-unit) * 1.5);
  }

  .header-info h1 {
    font-size: 1.85rem;
  }
  
  .affiliation {
    font-size: 1rem;
  }
  
  .location,
  .contact-email {
    font-size: 0.95rem;
  }
  
  .profile-image {
    width: 140px;
    height: 140px;
  }

  .social-links {
    justify-content: center;
  }
  
  .social-links a {
    width: 38px;
    height: 38px;
  }

  nav ul {
    justify-content: flex-start;
    padding: 0.6rem 0;
    gap: 0;
  }
  
  nav a {
    padding: 0.4rem 0.75rem;
    font-size: 0.85rem;
  }
  
  section {
    margin-bottom: calc(var(--spacing-unit) * 2.5);
  }
  
  h2 {
    font-size: 1.35rem;
  }
  
  h3 {
    font-size: 1.05rem;
  }
  
  .bio {
    font-size: 0.95rem;
  }
  
  .hiring-notice {
    flex-direction: column;
    align-items: flex-start;
    font-size: 0.9rem;
    padding: 0.75rem;
  }
  
  .news-item {
    flex-direction: column;
    gap: 0.5rem;
    padding: 0.85rem 0;
  }
  
  .news-date {
    align-self: flex-start;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
  }
  
  .news-content {
    font-size: 0.92rem;
  }
  
  .publication {
    padding: 1rem 1.15rem;
  }
  
  .pub-title {
    font-size: 0.98rem;
  }
  
  .pub-authors,
  .pub-venue {
    font-size: 0.88rem;
  }
  
  .pub-links a {
    font-size: 0.8rem;
    padding: 0.25rem 0.65rem;
  }
  
  .talk-item {
    font-size: 0.92rem;
    padding: 0.85rem 0;
  }
  
  .project {
    padding: 1rem 1.15rem;
  }
  
  .project-header {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .project-title {
    font-size: 0.98rem;
  }
  
  .project-links {
    align-self: flex-start;
  }
  
  .project-desc {
    font-size: 0.92rem;
  }
  
  .service-title,
  .service-content {
    font-size: 0.92rem;
  }

  .timeline-item {
    flex-direction: column;
    gap: 0.2rem;
    font-size: 0.92rem;
    padding: 0.65rem 0;
  }

  .timeline-year {
    margin-left: 0;
    font-size: 0.85rem;
  }
  
  footer {
    margin-top: calc(var(--spacing-unit) * 2.5);
    padding: calc(var(--spacing-unit) * 1.5) 0;
  }
  
  .footer-content {
    font-size: 0.85rem;
  }
  
  .visitor-map {
    max-width: 250px;
  }
}

/* ============================================
   Small Mobile (max-width: 374px)
   ============================================ */
@media (max-width: 374px) {
  body {
    font-size: 15px;
  }
  
  .header-info h1 {
    font-size: 1.7rem;
  }
  
  .profile-image {
    width: 120px;
    height: 120px;
  }
  
  nav a {
    padding: 0.35rem 0.6rem;
    font-size: 0.85rem;
  }
}

```

完成！已做以下调整：

## ✨ 更新内容

### 1. 照片阴影效果
- 添加了多层渐变阴影，带有淡蓝色调
- 悬停时阴影加深，效果更立体

### 2. 字体更黑更大

| 屏幕 | 之前 | 现在 |
|------|------|------|
| 大桌面 | 19px | **20px** |
| 普通桌面 | 18px | **19px** |
| 平板 | 17px | **18px** |
| 手机 | 16px | **17px** |

| 颜色 | 之前 | 现在 |
|------|------|------|
| 主文字 | `#141d2b` | `#0f1419` (接近纯黑) |
| 次文字 | `#374151` | `#2d3748` (深灰) |

### 3. 导航栏改为简洁风格
- 去掉白色背景框
- 改为**底部线条指示**样式
- 悬停/选中时显示蓝色下划线
- 更加简洁现代

刷新页面查看效果！

---

**User**

清理一下css里的无关代码，简洁一些。@index_new.html:22-46 主页我的照片和我的介绍尽量上下对齐。 这一行的按钮居中 @index_new.html:51-64。字体可以再黑一点 

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #0a0e14;
  --color-text-secondary: #232b38;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: center;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-image:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img { filter: brightness(0) invert(1); }
.social-links img { width: 22px; height: 22px; transition: filter 0.2s; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！CSS已精简并做了调整：

## ✅ 更新内容

### 1. CSS 精简
- 从 **846 行** 精简到 **~350 行**
- 移除冗余注释和重复代码
- 合并相似样式

### 2. 头像与介绍垂直居中
```css
.header-content {
  align-items: center;  /* 之前是 flex-start */
}
```

### 3. 导航栏按钮居中
```css
nav ul {
  justify-content: center;  /* 新增 */
}
```

### 4. 字体更黑
| 类型 | 之前 | 现在 |
|------|------|------|
| 主文字 | `#0f1419` | `#0a0e14` (接近纯黑) |
| 次文字 | `#2d3748` | `#232b38` (深灰黑) |

现在刷新浏览器查看效果！照片和文字居中对齐，导航栏按钮居中显示，整体字体更加清晰醒目。

```css
.header-content {
  align-items: center;  /* 之前是 flex-start */
}
```

```css
nav ul {
  justify-content: center;  /* 新增 */
}
```

---

**User**

@index_new.html:75 这种类型的文字字体再黑一点。 @index_new.html:22-46 照片和我的介绍再对齐一些。 @index_new.html:31-32 当鼠标放到这个按钮上的时候，换一个更简单的渐变动画，比如强化一下轮廓阴影即可，图标不用变化

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: center;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-image:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img { filter: brightness(0) invert(1); }
.social-links img { width: 22px; height: 22px; transition: filter 0.2s; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  margin-top: 0.25rem;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-image:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img { filter: brightness(0) invert(1); }
.social-links img { width: 22px; height: 22px; transition: filter 0.2s; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  margin-top: 0.25rem;
}

.profile-img {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  transition: all 0.2s;
}

.social-links a:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  transform: translateY(-2px);
}

.social-links a:hover img { filter: brightness(0) invert(1); }
.social-links img { width: 22px; height: 22px; transition: filter 0.2s; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  margin-top: 0.25rem;
}

.profile-img {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！已做以下调整：

## ✅ 更新内容

### 1. 文字颜色更黑
| 类型 | 之前 | 现在 |
|------|------|------|
| 主文字 | `#0a0e14` | `#080b10` |
| 次文字 (bio等) | `#232b38` | `#1a2130` (更深) |

### 2. 头像与介绍对齐
- 改为 `align-items: flex-start` 让照片顶部与姓名对齐
- 缩小间距为 `2.5rem`，视觉上更紧凑

### 3. 社交按钮悬停效果简化
**之前**: 背景变蓝 + 图标变白
**现在**: 
- 边框变为浅蓝色
- 添加蓝色阴影光晕
- 轻微上移
- 图标保持原样不变

```css
.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}
```

刷新页面查看效果！悬停时会有简洁的蓝色阴影光晕效果。

```css
.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}
```

---

**User**

我的照片的位置往下移，上端和Haoli Bai大标题对齐，下端和 @index_new.html:30 的位置对齐

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 220px; height: 220px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
.profile-image {
  width: 180px;
  min-height: 180px;
  height: auto;
  align-self: stretch;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}
```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 170px; height: 170px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; height: 140px; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-img:hover {
  transform: translateY(-4px);
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

让我修复那个替换错误：

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: stretch;
}

.profile-image {
  width: 180px;
  min-height: 180px;
  height: auto;
  align-self: stretch;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！照片现在会自动拉伸以匹配右侧内容的高度：

## ✅ 更新内容

### 照片对齐调整
```css
.profile-image {
  width: 180px;
  min-height: 180px;
  height: auto;
  align-self: stretch;  /* 拉伸以匹配右侧高度 */
  object-fit: cover;    /* 保持比例裁剪填充 */
}
```

现在照片会：
- **上端** 与 "Haoli Bai" 标题顶部对齐
- **下端** 与 social-links 底部对齐
- 高度自动适应右侧内容
- 保持良好的图片比例（使用 cover 裁剪）

同时移除了悬停时的上移动画，只保留阴影变化，效果更简洁。

刷新页面查看效果！

```css
.profile-image {
  width: 180px;
  min-height: 180px;
  height: auto;
  align-self: stretch;  /* 拉伸以匹配右侧高度 */
  object-fit: cover;    /* 保持比例裁剪填充 */
}
```

---

**User**

照片不要裁剪，保持原来的横宽比

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  width: 180px;
  min-height: 180px;
  height: auto;
  align-self: stretch;
  border-radius: 8px;
  object-fit: cover;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;
}

.profile-image {
  width: 180px;
  height: auto;
  border-radius: 8px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 200px; min-height: 200px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！照片现在保持原始比例：

```css
.profile-image {
  width: 180px;
  height: auto;           /* 高度自适应 */
  object-fit: contain;    /* 保持原比例，不裁剪 */
}
```

照片会：
- 宽度固定 180px
- 高度按原始比例自动计算
- 上端与标题对齐
- 不会被裁剪

刷新页面查看效果！

```css
.profile-image {
  width: 180px;
  height: auto;           /* 高度自适应 */
  object-fit: contain;    /* 保持原比例，不裁剪 */
}
```

---

**User**

@style/main.css:58-76 解释一下这段代码，我来修改。

---

**Cursor**

好的，让我逐行解释这段代码：

```css
.profile-image {
  width: 180px;           /* 照片宽度固定为180像素 */
  height: auto;           /* 高度自动，按原图比例计算 */
  border-radius: 8px;     /* 圆角8像素 */
  object-fit: contain;    /* 保持原始比例，不裁剪 */
  flex-shrink: 0;         /* 在flex布局中不被压缩 */
  box-shadow:             /* 多层阴影效果 */
    0 4px 6px rgba(0, 0, 0, 0.07),      /* 浅层小阴影 */
    0 10px 20px rgba(0, 0, 0, 0.06),    /* 中层阴影 */
    0 20px 40px rgba(37, 99, 168, 0.1); /* 深层蓝色调阴影 */
  transition: box-shadow 0.3s;          /* 阴影变化动画0.3秒 */
}

.profile-image:hover {    /* 鼠标悬停时 */
  box-shadow:             /* 加深阴影 */
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}
```

### 常用属性值参考：

| 属性 | 可选值 | 说明 |
|------|--------|------|
| `object-fit` | `contain` | 保持比例，完整显示 |
| | `cover` | 保持比例，填充裁剪 |
| | `fill` | 拉伸填充 |
| `width` | `180px` / `200px` 等 | 改变宽度 |
| `height` | `auto` / `200px` 等 | auto=按比例，固定值=可能裁剪 |
| `border-radius` | `8px` / `50%` 等 | 50%=圆形 |

您想怎么修改？

```css
.profile-image {
  width: 180px;           /* 照片宽度固定为180像素 */
  height: auto;           /* 高度自动，按原图比例计算 */
  border-radius: 8px;     /* 圆角8像素 */
  object-fit: contain;    /* 保持原始比例，不裁剪 */
  flex-shrink: 0;         /* 在flex布局中不被压缩 */
  box-shadow:             /* 多层阴影效果 */
    0 4px 6px rgba(0, 0, 0, 0.07),      /* 浅层小阴影 */
    0 10px 20px rgba(0, 0, 0, 0.06),    /* 中层阴影 */
    0 20px 40px rgba(37, 99, 168, 0.1); /* 深层蓝色调阴影 */
  transition: box-shadow 0.3s;          /* 阴影变化动画0.3秒 */
}

.profile-image:hover {    /* 鼠标悬停时 */
  box-shadow:             /* 加深阴影 */
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}
```

---

**User**

我想修改照片的位置和大小，怎么办

---

**Cursor**

## 修改照片大小和位置

### 1. 修改大小
在 `.profile-image` 中调整 `width`：

```css
.profile-image {
  width: 200px;    /* 改大：200px, 220px 等 */
  /* width: 160px; 改小 */
  height: auto;    /* 保持比例 */
  /* ... 其他属性 ... */
}
```

### 2. 修改位置（垂直对齐）

在 `.header-content` 中调整 `align-items`：

```css
.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;  /* 顶部对齐（当前） */
  /* align-items: center;   居中对齐 */
  /* align-items: flex-end; 底部对齐 */
}
```

### 3. 照片单独调整位置

可以给 `.profile-image` 添加 `margin`：

```css
.profile-image {
  width: 180px;
  height: auto;
  margin-top: 10px;    /* 向下移动 */
  /* margin-top: -5px; 向上移动 */
  /* ... 其他属性 ... */
}
```

### 4. 调整与文字的间距

在 `.header-content` 中修改 `gap`：

```css
.header-content {
  gap: 3rem;    /* 增大间距 */
  /* gap: 2rem; 减小间距 */
}
```

---

您可以直接在 `style/main.css` 文件中修改这些值。如果需要我帮您应用修改，请切换到 **Agent 模式**。

```css
.profile-image {
  width: 200px;    /* 改大：200px, 220px 等 */
  /* width: 160px; 改小 */
  height: auto;    /* 保持比例 */
  /* ... 其他属性 ... */
}
```

```css
.header-content {
  display: flex;
  gap: 2.5rem;
  align-items: flex-start;  /* 顶部对齐（当前） */
  /* align-items: center;   居中对齐 */
  /* align-items: flex-end; 底部对齐 */
}
```

```css
.profile-image {
  width: 180px;
  height: auto;
  margin-top: 10px;    /* 向下移动 */
  /* margin-top: -5px; 向上移动 */
  /* ... 其他属性 ... */
}
```

```css
.header-content {
  gap: 3rem;    /* 增大间距 */
  /* gap: 2rem; 减小间距 */
}
```

---

**User**

我想让图片大一些，标题向右移动一些给图片放大一点点的空间

---

**Cursor**

## 修改方案

### 1. 放大图片
找到 `.profile-image`（约第58行），修改 `width`：

```css
.profile-image {
  width: 210px;    /* 从 180px 改为 210px */
  height: auto;
  /* ... 其余不变 ... */
}
```

### 2. 增加图片与标题的间距
找到 `.header-content`（约第53行），增大 `gap`：

```css
.header-content {
  display: flex;
  gap: 3rem;    /* 从 2.5rem 改为 3rem */
  align-items: flex-start;
}
```

### 3. 响应式断点也需要调整

**大屏幕**（约第420行）：
```css
@media (min-width: 1200px) {
  .profile-image { width: 230px; min-height: 200px; }
}
```

**平板**（约第428行）：
```css
@media (max-width: 1023px) {
  .profile-image { width: 180px; min-height: 160px; }
}
```

---

您可以直接在 CSS 文件中手动修改这些值，或切换到 **Agent 模式** 让我帮您自动应用。

```css
.profile-image {
  width: 210px;    /* 从 180px 改为 210px */
  height: auto;
  /* ... 其余不变 ... */
}
```

```css
.header-content {
  display: flex;
  gap: 3rem;    /* 从 2.5rem 改为 3rem */
  align-items: flex-start;
}
```

```css
@media (min-width: 1200px) {
  .profile-image { width: 230px; min-height: 200px; }
}
```

```css
@media (max-width: 1023px) {
  .profile-image { width: 180px; min-height: 160px; }
}
```

---

**User**

帮我处理吧

---

**Cursor**

```css
.header-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
}
```

```css
.profile-image {
  width: 210px;
  height: auto;
  border-radius: 8px;
  object-fit: contain;
  flex-shrink: 0;
```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 4rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 160px; min-height: 160px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 4rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.85rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 180px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

看起来您已经自己做了一些调整！我看到您已修改为：
- 图片宽度：`400px`
- 间距：`4rem`  
- 顶部边距：`margin-top: 25px`

我已帮您更新了响应式断点：
- 大屏幕：图片 `230px`
- 平板：图片 `180px`

当前效果应该已经符合您的需求了。刷新页面查看效果！如需进一步调整，随时告诉我。

---

**User**

标题 Haoli Bai的字体稍微小2号

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 180px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！标题字体已缩小：

- **之前**: `2.85rem`
- **现在**: `2.5rem`

刷新页面查看效果！

---

**User**

@index_new.html:26 字体稍微小两号

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  box-shadow: 
    0 6px 12px rgba(0, 0, 0, 0.1),
    0 15px 30px rgba(0, 0, 0, 0.08),
    0 25px 50px rgba(37, 99, 168, 0.14);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.6rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 180px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！标题字体已调整：

- **之前**: `2.85rem`
- **现在**: `2.6rem`

刷新查看效果！

---

**User**

@style/main.css:79-84 解释一下

---

**Cursor**

这段代码控制标题 "Haoli Bai (柏昊立)" 的样式：

```css
.header-info h1 {
  font-family: var(--font-serif);  /* 使用衬线字体 Playfair Display */
  font-size: 2.5rem;               /* 字体大小 2.5rem ≈ 40px */
  font-weight: 700;                /* 字重700 = 粗体 */
  margin-bottom: 0rem;             /* 标题下方间距为0 */
}
```

### 属性说明：

| 属性 | 当前值 | 说明 |
|------|--------|------|
| `font-family` | `var(--font-serif)` | 引用CSS变量，即 Playfair Display 字体 |
| `font-size` | `2.5rem` | 字体大小（1rem = 16px，所以约40px） |
| `font-weight` | `700` | 粗细：400=正常，600=半粗，**700=粗体** |
| `margin-bottom` | `0rem` | 与下方内容的间距（您改成了0） |

### 如果想调整：
- 字体更大：`font-size: 2.8rem;`
- 字体更小：`font-size: 2.2rem;`
- 更细：`font-weight: 600;`
- 增加下方间距：`margin-bottom: 0.5rem;`

```css
.header-info h1 {
  font-family: var(--font-serif);  /* 使用衬线字体 Playfair Display */
  font-size: 2.5rem;               /* 字体大小 2.5rem ≈ 40px */
  font-weight: 700;                /* 字重700 = 粗体 */
  margin-bottom: 0rem;             /* 标题下方间距为0 */
}
```

---

**User**

@style/main.css @index.html 添加一个鼠标碰到照片，照片微微上浮的效果

---

**Cursor**

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: box-shadow 0.3s;
}

.profile-image:hover {
  transform: translateY(-6px);
  box-shadow: 
    0 8px 16px rgba(0, 0, 0, 0.1),
    0 18px 35px rgba(0, 0, 0, 0.08),
    0 30px 55px rgba(37, 99, 168, 0.15);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 0rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 180px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

```css
/* Academic Personal Website - Haoli Bai */

:root {
  --color-bg: #f7f9fc;
  --color-text: #080b10;
  --color-text-secondary: #1a2130;
  --color-accent: #2563a8;
  --color-accent-light: #60a5c8;
  --color-border: #d8e3ed;
  --color-card-bg: #ffffff;
  --color-tag: #e8f1f8;
  --font-serif: 'Playfair Display', Georgia, serif;
  --font-sans: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  --max-width: 960px;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: var(--font-sans);
  font-size: 19px;
  line-height: 1.75;
  color: var(--color-text);
  background: var(--color-bg);
  -webkit-font-smoothing: antialiased;
}

body::before {
  content: '';
  position: fixed;
  inset: 0;
  background: 
    radial-gradient(circle at 15% 25%, rgba(37, 99, 168, 0.04) 0%, transparent 45%),
    radial-gradient(circle at 85% 75%, rgba(96, 165, 200, 0.03) 0%, transparent 45%);
  pointer-events: none;
  z-index: -1;
}

.container {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header */
header {
  padding: 4rem 0 3rem;
  animation: fadeInUp 0.8s ease-out;
}

.header-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
}

.profile-image {
  width: 400px;
  height: auto;
  border-radius: 8px;
  margin-top: 25px;
  object-fit: contain;
  flex-shrink: 0;
  box-shadow: 
    0 4px 6px rgba(0, 0, 0, 0.07),
    0 10px 20px rgba(0, 0, 0, 0.06),
    0 20px 40px rgba(37, 99, 168, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-6px);
  box-shadow: 
    0 8px 16px rgba(0, 0, 0, 0.1),
    0 18px 35px rgba(0, 0, 0, 0.08),
    0 30px 55px rgba(37, 99, 168, 0.15);
}

.header-info h1 {
  font-family: var(--font-serif);
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 0rem;
}

.affiliation {
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.contact-email {
  font-size: 1rem;
  color: var(--color-text-secondary);
  margin-bottom: 1.25rem;
}

/* Social Links */
.social-links {
  display: flex;
  gap: 0.75rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: all 0.2s;
}

.social-links a:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 12px rgba(37, 99, 168, 0.2);
  transform: translateY(-2px);
}

.social-links img { width: 22px; height: 22px; }

/* Navigation */
nav {
  position: sticky;
  top: 0;
  background: rgba(247, 249, 252, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--color-border);
  z-index: 100;
  margin-bottom: 2rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 0;
}

nav a {
  display: block;
  padding: 0.5rem 1.1rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  text-decoration: none;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
  border-bottom-color: var(--color-accent);
}

/* Sections */
section {
  margin-bottom: 3.5rem;
  animation: fadeInUp 0.6s ease-out backwards;
}

h2 {
  font-family: var(--font-serif);
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1.25rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--color-accent-light);
  display: inline-block;
}

h3 {
  font-family: var(--font-serif);
  font-size: 1.25rem;
  font-weight: 600;
  margin: 1.5rem 0 0.75rem;
}

/* Bio */
.bio {
  font-size: 1.05rem;
  line-height: 1.85;
  color: var(--color-text-secondary);
}

.bio a {
  color: var(--color-accent);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.bio a:hover { border-bottom-color: var(--color-accent); }
.bio p + p { margin-top: 1rem; }

.hiring-notice {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, #eff6ff, #e0f0ff);
  border: 1px solid #a5c8e8;
  border-radius: 8px;
  padding: 0.75rem 1rem;
  margin-top: 1rem;
  font-size: 1rem;
}

/* News */
.news-list { list-style: none; }

.news-item {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
}

.news-item:last-child { border-bottom: none; }

.news-date {
  flex-shrink: 0;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-accent);
  background: var(--color-tag);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  height: fit-content;
}

.news-content {
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.65;
}

.news-content a { color: var(--color-accent); text-decoration: none; }
.news-content a:hover { text-decoration: underline; }

/* Publications */
.pub-note {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  font-style: italic;
  margin-bottom: 1.5rem;
}

.publication {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
  transition: all 0.2s;
}

.publication:hover {
  border-color: var(--color-accent-light);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.pub-title a { color: var(--color-text); text-decoration: none; transition: color 0.2s; }
.pub-title a:hover { color: var(--color-accent); }

.pub-authors {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
  line-height: 1.55;
}

.pub-venue {
  font-size: 0.95rem;
  font-style: italic;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.pub-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.pub-links a {
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.3rem 0.85rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.pub-links a:hover { background: var(--color-accent); color: white; }

/* Talks */
.talks-list { list-style: none; }

.talk-item {
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
  color: var(--color-text-secondary);
  line-height: 1.6;
}

.talk-item:last-child { border-bottom: none; }
.talk-item a { color: var(--color-accent); text-decoration: none; }
.talk-item a:hover { text-decoration: underline; }

/* Projects */
.project {
  background: var(--color-card-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 1.25rem 1.5rem;
  margin-bottom: 1rem;
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 1rem;
}

.project-title { font-size: 1.05rem; font-weight: 600; }
.project-links { display: flex; gap: 0.5rem; flex-shrink: 0; }

.project-links a {
  font-size: 0.85rem;
  color: var(--color-accent);
  text-decoration: none;
  padding: 0.25rem 0.7rem;
  background: var(--color-tag);
  border-radius: 4px;
  transition: all 0.2s;
}

.project-links a:hover { background: var(--color-accent); color: white; }
.project-desc { font-size: 1rem; color: var(--color-text-secondary); line-height: 1.65; }

/* Services */
.service-category { margin-bottom: 1rem; }
.service-title { font-weight: 600; font-size: 1rem; margin-bottom: 0.25rem; }
.service-content { font-size: 1rem; color: var(--color-text-secondary); }

/* Timeline */
.timeline-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--color-border);
  font-size: 1rem;
}

.timeline-item:last-child { border-bottom: none; }
.timeline-title a { color: var(--color-accent); text-decoration: none; }
.timeline-title a:hover { text-decoration: underline; }
.timeline-year { color: var(--color-text-secondary); flex-shrink: 0; margin-left: 1rem; }

/* Footer */
footer {
  margin-top: 4rem;
  padding: 2rem 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}

.footer-content { font-size: 0.9rem; color: var(--color-text-secondary); margin-bottom: 1.5rem; }
.footer-content a { color: var(--color-accent); text-decoration: none; }
.footer-content a:hover { text-decoration: underline; }
.visitor-map { max-width: 300px; margin: 0 auto; }

/* Animation */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Large Desktop */
@media (min-width: 1200px) {
  :root { --max-width: 1000px; }
  body { font-size: 20px; }
  .header-info h1 { font-size: 3.1rem; }
  .profile-image { width: 230px; }
  h2 { font-size: 1.85rem; }
}

/* Tablet */
@media (max-width: 1023px) {
  :root { --max-width: 720px; }
  body { font-size: 18px; }
  .container { padding: 0 1.5rem; }
  .header-info h1 { font-size: 2.35rem; }
  .profile-image { width: 180px; }
}

/* Mobile */
@media (max-width: 767px) {
  body { font-size: 17px; }
  .container { padding: 0 1rem; }
  header { padding: 2.5rem 0 2rem; }
  
  .header-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
  }

  .header-info h1 { font-size: 1.85rem; }
  .affiliation { font-size: 1rem; }
  .location, .contact-email { font-size: 0.95rem; }
  .profile-image { width: 140px; min-height: 140px; height: auto; }
  .social-links { justify-content: center; }
  .social-links a { width: 38px; height: 38px; }

  nav ul { justify-content: flex-start; padding: 0.6rem 0; gap: 0; overflow-x: auto; }
  nav a { padding: 0.4rem 0.75rem; font-size: 0.85rem; }
  
  section { margin-bottom: 2.5rem; }
  h2 { font-size: 1.35rem; }
  h3 { font-size: 1.05rem; }
  .bio { font-size: 0.95rem; }
  
  .hiring-notice { flex-direction: column; align-items: flex-start; font-size: 0.9rem; padding: 0.75rem; }
  .news-item { flex-direction: column; gap: 0.5rem; padding: 0.85rem 0; }
  .news-date { align-self: flex-start; font-size: 0.8rem; padding: 0.2rem 0.6rem; }
  .news-content { font-size: 0.92rem; }
  
  .publication { padding: 1rem 1.15rem; }
  .pub-title { font-size: 0.98rem; }
  .pub-authors, .pub-venue { font-size: 0.88rem; }
  .pub-links a { font-size: 0.8rem; padding: 0.25rem 0.65rem; }
  
  .talk-item { font-size: 0.92rem; padding: 0.85rem 0; }
  .project { padding: 1rem 1.15rem; }
  .project-header { flex-direction: column; gap: 0.5rem; }
  .project-title { font-size: 0.98rem; }
  .project-links { align-self: flex-start; }
  .project-desc { font-size: 0.92rem; }
  .service-title, .service-content { font-size: 0.92rem; }
  
  .timeline-item { flex-direction: column; gap: 0.2rem; font-size: 0.92rem; padding: 0.65rem 0; }
  .timeline-year { margin-left: 0; font-size: 0.85rem; }
  
  footer { margin-top: 2.5rem; padding: 1.5rem 0; }
  .footer-content { font-size: 0.85rem; }
  .visitor-map { max-width: 250px; }
}

/* Small Mobile */
@media (max-width: 374px) {
  body { font-size: 15px; }
  .header-info h1 { font-size: 1.7rem; }
  .profile-image { width: 120px; min-height: 120px; }
  nav a { padding: 0.35rem 0.6rem; font-size: 0.85rem; }
}

```

完成！添加了照片悬停上浮效果：

```css
.profile-image {
  transition: transform 0.3s ease, box-shadow 0.3s ease;  /* 添加平滑过渡 */
}

.profile-image:hover {
  transform: translateY(-6px);  /* 上浮6像素 */
  box-shadow: /* 阴影也随之加深 */
    0 8px 16px rgba(0, 0, 0, 0.1),
    0 18px 35px rgba(0, 0, 0, 0.08),
    0 30px 55px rgba(37, 99, 168, 0.15);
}
```

现在鼠标悬停照片时会：
- 向上浮动 6px
- 阴影加深加大
- 过渡动画 0.3 秒

刷新页面查看效果！

```css
.profile-image {
  transition: transform 0.3s ease, box-shadow 0.3s ease;  /* 添加平滑过渡 */
}

.profile-image:hover {
  transform: translateY(-6px);  /* 上浮6像素 */
  box-shadow: /* 阴影也随之加深 */
    0 8px 16px rgba(0, 0, 0, 0.1),
    0 18px 35px rgba(0, 0, 0, 0.08),
    0 30px 55px rgba(37, 99, 168, 0.15);
}
```

