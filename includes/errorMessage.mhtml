<div class="toast-container position-fixed top-0 end-0 p-5 mt-5">
    <div id="liveToast" class="toast align-items-center 
        <?php echo ($_SESSION['status_type'] == 'success') ? 'text-bg-success' : 'text-bg-danger'; ?>        
        border-0" 
        role="alert" aria-live="assertive" aria-atomic="true">
        
        <div class="d-flex">
            <div class="toast-body">
                <b>
                    <?php
                    if (isset($_SESSION['status'])) {
                        echo $_SESSION['status'];
                    ?>
                    <script>
                        const toastTrigger = document.getElementById('liveToastBtn');
                        const toastLiveExample = document.getElementById('liveToast');
                        const toastBootstrap = bootstrap.Toast.getOrCreateInstance(toastLiveExample);
                        toastBootstrap.show();
                    </script>
                    <?php
                        unset($_SESSION['status']);
                        unset($_SESSION['status_type']);
                    }
                    ?>
                </b>
            </div>
            <button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast" aria-label="Close"></button>
        </div>
    </div>
</div>
