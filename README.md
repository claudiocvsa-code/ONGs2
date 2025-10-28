# ONGs2
ONGs2
<p>&copy; 2025 ONGConecta. Todos os direitos reservados.</p>
  </footer>

  <script src="js/main.js"></script>
</body>
</html>
``

4. Navegação responsiva com submenu e menu hambúrguer — trecho em CSS/JS

CSS (em style.css):

css
.main-nav { display: flex; align-items: center; justify-content: space-between; padding: var(--space-16); }
.nav-links { display: flex; gap: var(--space-24); }
.hamburger { display: none; background: none; border: none; }
@media (max-width: 768px) {
  .nav-links { display: none; flex-direction: column; }
  .hamburger { display: block; }
}


JavaScript (em main.js):

js
const hamburger = document.querySelector('.hamburger');
const navLinks = document.querySelector('.nav-links');

hamburger.addEventListener('click', () => {
  navLinks.classList.toggle('show');
});



5. Componentes de Interface — Exemplos

Botão com estados (hover, focus, active, disabled):

css
.btn {
  padding: var(--space-16) var(--space-24);
  font-size: var(--font-size-md);
  background: var(--color-primary);
  color: var(--color-neutral-100);
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background 0.3s;
}
.btn:hover { background: var(--color-secondary); }
.btn:focus { outline: 2px solid var(--color-accent-success); }

.btn:active { background: var(--color-primary-dark); }
.btn:disabled { background: var(--color-neutral-300); color: var(--color-neutral-400); cursor: not-allowed; }


Card responsivo para projetos:

html
<article class="card">
  <img src="assets/img/projeto1.jpg" alt="Projeto 1">
  <div class="card-content" style="padding: var(--space-16);">
    <h3 style="font-size: var(--font-size-lg);">Projeto X</h3>
    <p style="font-size: var(--font-size-md);">Descrição breve...</p>
    <button class="btn">Saiba mais</button>
  </div>
</article>


css
.card {
  border: 1px solid var(--color-neutral-300);
  border-radius: 8px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.card img { width: 100%; height: auto; }
@media (min-width: 600px) {
  .card { flex-direction: row; }
  .card-content { padding: var(--space-24); }
}


Formulário com validação visual:

html
<form id="voluntario-form">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" required>
  <span class="error-message" aria-live="polite"></span>

  <label for="email">E‑mail:</label>
  <input type="email" id="email" required>
  <span class="error-message" aria-live="polite"></span>

  <button type="submit" class="btn">Enviar</button>
</form>


js
/* Grid customizado (12 colunas) */
  --grid-columns: 12;
}


3. HTML — Página inicial (index.html)

html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Plataforma ONGConecta</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header class="site-header">
    <nav class="main-nav">
      <a href="index.html" class="logo">ONGConecta</a>
      <button class="hamburger" aria-label="Abrir menu">
        <img src="assets/icons/menu.svg" alt="Menu">
      </button>
      <ul class="nav-links">
        <li><a href="index.html">Início</a></li>
        <li><a href="projetos.html">Projetos</a></li>
        <li><a href="cadastro.html">Cadastre‑se</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="intro" style="padding: var(--space-32);">
      <h1 style="font-size: var(--font-size-xxl);">Conectando pessoas com causas sociais</h1>
      <p style="font-size: var(--font-size-md);">Nossa plataforma permite que ONGs gerenciem projetos, captem recursos e envolvam voluntários.</p>
    </section>
  </main>

  <footer class="site-footer" style="padding: var(--space-16); text-align: center; background: var(--color-neutral-200);">

document.getElementById('voluntario-form').addEventListener('submit', f…
