---
layout: none
permalink: slide.html
---
<!--New Experiment-->
<h2>Available Travel Packages</h2>

<div class="package-grid">
  {% for product in site.data.products %}
    <div class="package-card">
      <h3>{{ product.name }}</h3>
      
      <div class="package-price">${{ product.price }}</div>
      
      <p class="package-qty">
        {% if product.qty > 0 %}
          Spots remaining: {{ product.qty }}
        {% else %}
          <strong style="color: red;">Sold Out!</strong>
        {% endif %}
      </p>
      
      <button style="width: 100%; padding: 10px; cursor: pointer;">Book Now</button>
    </div>
  {% else %}
    <p>No travel packages are currently available. Please check back later!</p>
  {% endfor %}
</div>
<!--end New Experiment-->