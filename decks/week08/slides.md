<section class="title-slide">
Semana 8 | Presentaciones Finales
<div class="subtitle">Mercados y Riesgos Financieros • <em>Noviembre 26, 2025</em></div>
</section>

---

## Agenda
1. Presentaciones Finales
2. Cierre del Modulo

---

## Semana 8: Presentaciones Finales

---

<section>
  <h2>RANDOM WHEEL</h2>

  <div class="wheel-wrapper">
    <div class="wheel-pointer">▼</div>
    <div class="wheel"></div>
  </div>

  <button class="spin-btn">Spin</button>
  <p class="wheel-result"></p>

  <div class="wheel-lists">
    <div>
      <h3>REMAINING</h3>
      <ul class="remaining-list"></ul>
    </div>
    <div>
      <h3>USED</h3>
      <ul class="used-list"></ul>
    </div>
  </div>

  <script>
    (function () {
      // Scope everything to THIS slide
      const root          = document.currentScript.parentElement;
      const wheel         = root.querySelector('.wheel');
      const spinBtn       = root.querySelector('.spin-btn');
      const resultEl      = root.querySelector('.wheel-result');
      const remainingList = root.querySelector('.remaining-list');
      const usedList      = root.querySelector('.used-list');

      if (!wheel || !spinBtn) return;

      // ==== EDIT YOUR LABELS HERE ====
      const labels = [
        'Grupo 1',
        'Grupo 2',
        'Grupo 3',
        'Grupo 4',
        'Grupo 5',
        'Grupo 6',
        'Grupo 7',
        'Grupo 8',
        'Grupo 9'
      ];

      const n = labels.length;
      const segmentAngle = 360 / n;

      let availableIndices = labels.map((_, i) => i);
      const usedIndices = [];

      function buildWheelBackground() {
        const parts = [];
        for (let i = 0; i < n; i++) {
          const start = i * segmentAngle;
          const end   = (i + 1) * segmentAngle;
          const hue   = Math.round((360 * i) / n);
          parts.push(`hsl(${hue}, 70%, 60%) ${start}deg ${end}deg`);
        }
        return `conic-gradient(${parts.join(',')})`;
      }

      wheel.style.background = buildWheelBackground();

      function renderLists() {
        remainingList.innerHTML = '';
        usedList.innerHTML = '';

        availableIndices.forEach(i => {
          const li = document.createElement('li');
          li.textContent = labels[i];
          remainingList.appendChild(li);
        });

        usedIndices.forEach(i => {
          const li = document.createElement('li');
          li.textContent = labels[i];
          li.classList.add('used');
          usedList.appendChild(li);
        });
      }

      renderLists();

      let currentRotation = 0;
      let isSpinning = false;

      spinBtn.addEventListener('click', () => {
        if (isSpinning) return;

        if (availableIndices.length === 0) {
          resultEl.textContent = 'All segments already used.';
          spinBtn.disabled = true;
          return;
        }

        isSpinning = true;
        resultEl.textContent = '';

        const r = Math.floor(Math.random() * availableIndices.length);
        const chosenIndex = availableIndices[r];

        // remove from remaining, add to used
        availableIndices.splice(r, 1);
        usedIndices.push(chosenIndex);

        const fullTurns = 3 + Math.floor(Math.random() * 3);
        const segmentCenter = chosenIndex * segmentAngle + segmentAngle / 2;
        const targetAngle = 360 - segmentCenter;
        const finalRotation = fullTurns * 360 + targetAngle;

        wheel.style.transition = 'transform 4s cubic-bezier(0.25, 0.1, 0.25, 1)';
        wheel.style.transform  = `rotate(${finalRotation}deg)`;

        const onEnd = () => {
          wheel.removeEventListener('transitionend', onEnd);
          currentRotation = finalRotation % 360;
          wheel.style.transition = 'none';
          wheel.style.transform  = `rotate(${currentRotation}deg)`;

          renderLists();

          resultEl.textContent = `Result: ${labels[chosenIndex]}`;
          isSpinning = false;

          if (availableIndices.length === 0) {
            spinBtn.disabled = true;
          }
        };

        wheel.addEventListener('transitionend', onEnd);
      });
    })();
  </script>
</section>


---

## Cierre del curso

---

## Contacto

aariofrio@utpl.edu.ec

www.linkedin.com/in/andres-riofrio-lara