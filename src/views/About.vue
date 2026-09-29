<template>
  <div class="about-page">
    <div class="about-header">
      <h1>About Gatherly</h1>
      <p>We connect people through amazing curated events and shared experiences.</p>
    </div>
  </div>
</template>

<style scoped>
.about-page {
  animation: fadeIn 0.5s ease;
  max-width: 800px;
  margin: 0 auto;
}
.about-header {
  text-align: center;
  margin-bottom: 4rem;
  padding: 4rem 2rem;
  background: #fdfdfd;
  border-radius: 20px;
  border: 1px solid #f0f0f0;
}
.about-header h1 {
  font-size: 3rem;
  color: #1c1948;
  margin-bottom: 1rem;
}
.about-header p {
  font-size: 1.2rem;
  color: #666;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>

<style scoped>
.contact-page {
  animation: fadeIn 0.5s ease;
  max-width: 900px;
  margin: 0 auto;
}

.contact-header {
  text-align: center;
  margin-bottom: 3rem;
  padding: 3rem 2rem;
  background: #fdfdfd;
  border-radius: 20px;
  border: 1px solid #f0f0f0;
}

.contact-header h1 {
  font-size: 2.8rem;
  color: #1c1948;
  margin-bottom: 1rem;
}

.contact-header p {
  font-size: 1.1rem;
  color: #666;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 2.5rem;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.info-card {
  background: white;
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 4px 15px rgba(0,0,0,0.02);
}

.info-card h3 {
  color: #1c1948;
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
}

.info-card p {
  color: #666;
  line-height: 1.6;
}

.contact-form-wrapper {
  background: white;
  padding: 2.5rem;
  border-radius: 16px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 4px 15px rgba(0,0,0,0.02);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: #1c1948;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.8rem 1rem;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  font-family: inherit;
  font-size: 1rem;
  transition: border-color 0.3s;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #6644ff;
}

.btn-submit {
  background: #6644ff;
  color: white;
  border: none;
  padding: 0.8rem 2rem;
  border-radius: 8px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s, transform 0.2s;
  width: 100%;
}

.btn-submit:hover {
  background: #5533ee;
  transform: translateY(-2px);
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>