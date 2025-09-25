---
layout: default
title: 菜单收藏
permalink: /menus/
---

<div class="blog-posts">
  {% for menu in site.menus %}
    <div class="post-card">
      <h3><span class="menu-icon">🍽</span>{{ menu.title }}</h3>
      <div class="date">{{ menu.date | date: "%Y年%m月%d日" }}</div>
      <div class="description">{{ menu.description }}</div>
      <div class="preview">
        <strong>特色菜品：</strong><br>
        {% for dish in menu.featured_dishes %}
          • {{ dish }}<br>
        {% endfor %}
      </div>
      <a href="{{ menu.url }}" class="view-btn">查看菜单</a>
    </div>
  {% endfor %}
</div>

<style>
  .blog-posts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
    margin-top: 40px;
  }
  
  .post-card {
    background: rgba(255, 255, 255, 0.8);
    border-radius: 12px;
    padding: 25px;
    box-shadow: 0 5px 15px rgba(139, 69, 19, 0.1);
    transition: all 0.3s ease;
    border: 1px solid rgba(212, 163, 115, 0.2);
    position: relative;
    overflow: hidden;
  }
  
  .post-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(90deg, #d4a373, #8b4513);
  }
  
  .post-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(139, 69, 19, 0.2);
    border-color: #d4a373;
  }
  
  .post-card h3 {
    font-size: 1.3rem;
    font-weight: 500;
    color: #2c1810;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
  }
  
  .post-card .date {
    font-size: 0.9rem;
    color: #8b4513;
    margin-bottom: 15px;
    font-weight: 300;
  }
  
  .post-card .description {
    font-size: 0.85rem;
    color: #5c4a3a;
    line-height: 1.5;
    margin-bottom: 20px;
  }
  
  .post-card .preview {
    font-size: 0.8rem;
    color: #8b4513;
    background: rgba(212, 163, 115, 0.1);
    padding: 10px;
    border-radius: 6px;
    margin-bottom: 20px;
    border-left: 3px solid #d4a373;
  }
  
  .post-card .view-btn {
    display: inline-block;
    background: linear-gradient(135deg, #d4a373, #8b4513);
    color: white;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 500;
    transition: all 0.3s ease;
    text-align: center;
    width: 100%;
  }
  
  .post-card .view-btn:hover {
    background: linear-gradient(135deg, #8b4513, #d4a373);
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(139, 69, 19, 0.3);
  }
  
  .menu-icon {
    font-size: 1.2rem;
    margin-right: 8px;
    color: #d4a373;
  }
  
  @media (max-width: 768px) {
    .blog-posts {
      grid-template-columns: 1fr;
      gap: 20px;
    }
  }
</style>
