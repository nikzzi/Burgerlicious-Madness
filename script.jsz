let currentSlide = 0;

const slides = document.querySelectorAll('.slide');
const sliderContainer = document.querySelector('.slider-container');
const indicators = document.querySelectorAll('.indicator');
const totalSlides = slides.length;

function showSlide(index) {
  if (index < 0) index = totalSlides - 1;
  if (index >= totalSlides) index = 0;

  sliderContainer.style.transform = `translateX(-${index * 100}%)`;

  indicators.forEach((dot, i) => {
    dot.classList.toggle('active', i === index);
  });

  currentSlide = index;
  resetAutoSlide();
}

document.querySelector('.prev').addEventListener('click', () => {
  showSlide((currentSlide - 1 + totalSlides) % totalSlides);
});

document.querySelector('.next').addEventListener('click', () => {
  showSlide((currentSlide + 1) % totalSlides);
});

indicators.forEach((dot, i) => {
  dot.addEventListener('click', () => {
    showSlide(i);
  });
});

let autoSlide = setInterval(() => {
  showSlide((currentSlide + 1) % totalSlides);
}, 5000);

function resetAutoSlide() {
  clearInterval(autoSlide);
  autoSlide = setInterval(() => {
    showSlide((currentSlide + 1) % totalSlides);
  }, 5000);
}

const menu = document.querySelector('a[href="#menu"]');
const locations = document.querySelector('a[href="#locations"]');
const contact = document.querySelector('a[href="#contact"]');
const divider1 = document.querySelector('.divider1');
const divider2 = document.querySelector('.divider2');

menu.addEventListener('mouseenter', () => {
  divider1.classList.add('divider-hover');
});
menu.addEventListener('mouseleave', () => {
  divider1.classList.remove('divider-hover');
});

locations.addEventListener('mouseenter', () => {
  divider1.classList.add('divider-hover');
  divider2.classList.add('divider-hover');
});
locations.addEventListener('mouseleave', () => {
  divider1.classList.remove('divider-hover');
  divider2.classList.remove('divider-hover');
});

contact.addEventListener('mouseenter', () => {
  divider2.classList.add('divider-hover');
});
contact.addEventListener('mouseleave', () => {
  divider2.classList.remove('divider-hover');
});

document.addEventListener('DOMContentLoaded', () => {
  const fadingElements = document.querySelectorAll('.location-pin, .footer-logo-img, .main-nav, .footer-section, .location-text, .search-bar, .icon, .location-text, .button-container, .menu-item');

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target); 
    }
  });
}, {
  threshold: 0.1
});

  fadingElements.forEach(el => observer.observe(el));
});

window.addEventListener('load', () => {
  document.getElementById('popup-advert').style.display = 'flex';
});

function closePopup() {
  document.getElementById('popup-advert').style.display = 'none';
}


