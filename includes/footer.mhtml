

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
    crossorigin="anonymous"></script>
    <script>
        function setLightMode() {
            document.body.classList.remove('dark-mode');
            document.body.classList.add('light-mode');
            localStorage.setItem('theme', 'light');
        }

        function setDarkMode() {
            document.body.classList.remove('light-mode');
            document.body.classList.add('dark-mode');
            localStorage.setItem('theme', 'dark');
        }

        function setAutoMode() {
            document.body.classList.remove('dark-mode', 'light-mode');
            if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
                document.body.classList.add('dark-mode');
            } else {
                document.body.classList.add('light-mode');
            }
            localStorage.setItem('theme', 'auto');
        }

        // Load the theme from local storage on page load
        window.onload = function() {
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'dark') {
                setDarkMode();
            } else if (savedTheme === 'light') {
                setLightMode();
            } else {
                setAutoMode();
            }
        }

        // Listen to system theme changes for auto mode
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', (e) => {
            if (localStorage.getItem('theme') === 'auto') {
                if (e.matches) {
                    setDarkMode();
                } else {
                    setLightMode();
                }
            }
        });
    </script> 

    <footer class="container-fluid text-center mb-3" style="color: rgba(130, 130, 130, 1.0);">
        <hr class="footer-separator" style="margin-top: 0;">
        <a href="privacy.php" style="color: rgba(130, 130, 130, 1.0);">Privacy Policy</a> • <a
            href="terms.php" style="color: rgba(130, 130, 130, 1.0);">Terms of Use</a><br>&copy; 2024
            Darshana Education. All
            Rights
            Reserved.
    </footer> 

</body>

</html>
