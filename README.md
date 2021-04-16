<article>
        <section class="columns-desktop">
          <div class="pie">
            <img src="images/apple-pie.png" alt="Apple pie">
            <div class="columns">
              <div class="title">Apple Pie</div>
              <div class="price">$12.95</div>
          </div>
          <p class="desc">Our famous apple pie</p>
          <button data-order="apple-pie">Order</button>
          </div>
          <div class="pie">
            <img src="images/cherry-pie.png" alt="Cherry pie">
            <div class="columns">
              <div class="title">Cherry Pie</div>
              <div class="price">$15.95</div>
          </div>
          <p class="desc">A summer classic!</p>
          <button data-order="cherry-pie">Order</button>
          </div>
        </section>
      </article>
    </main>
    <footer>
      <nav>
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="pies.html">Pies</a></li>
          <li><a href="contact.html">Contact</a></li>
        </ul>
      </nav>
    </footer>
</body>
  <script>
    window.addEventListener("DOMContentLoaded", function (e) {
      const orderButtons = document.querySelectorAll("data-order");

      orderButtons.forEach(function (button) {

        button.addEventListener("click", function (e) {
          const button = e.currentTarget;
          const button = button.parentNode;

          const order = {
            id: button.getAtrribute("data-order"),
            title: container.querySelector(".title").innerText,
            price: container.querySelector(".price").innerText,
            desc: container.querySelector(".desc").innerText,
          };

            localStorage.setItem("order", JSON.stringify(order));

            const url = window.location.href.replace("pies.html", "order.html");

        });
      });

    });
  </script>
