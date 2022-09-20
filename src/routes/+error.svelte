<script>
    import { page } from '$app/stores';
  </script>

<div class="row">
    <div class="col-6 offset-3">
        <div class="alert alert-danger" role="alert">
            <h4 class="alert-heading">{$page.status}</h4>
            {#if (process.env.NODE_ENV !== 'production' && $page.error)} 
            <p>{$page.error.message}</p>
            {/if}
          </div>
    </div>
  </div>