# Vue

[Back](./..)

- [Create Vue Component using CLI](#create-vue-component-using-cli-️)

## Create Vue Component using CLI ([⬆️](#vue))

Run this command in your Laravel Project.

```sh
php artisan make:command MakeVueCommand
```

Then goto **app/Console/Commands/MakeVueCommand.php** directory, use this following code:

```php
<?php

namespace App\Console\Commands;

use Illuminate\Console\Command;
use Illuminate\Support\Facades\File;

class MakeVueCommand extends Command
{
    /**
     * The name and signature of the console command.
     *
     * @var string
     */
    protected $signature = 'make:vue {name}';

    /**
     * The console command description.
     *
     * @var string
     */
    protected $description = 'Create a new Vue component';

    /**
     * Execute the console command.
     */
    public function handle()
    {
        $name = $this->argument('name');
        $componentName = ucfirst($name);
        $directory = resource_path("js/Components");
        $path = "{$directory}/{$componentName}.vue";

        // Ensure directory exists
        File::ensureDirectoryExists($directory);

        if (File::exists($path)) {
            $this->error('Component already exists!');
            return;
        }

        $template = <<<EOT
<template>
  <div>
    <!-- Your template here -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      // your data here
    }
  },
  methods: {
    // your methods here
  }
}
</script>

<style scoped>

</style>
EOT;

        File::put($path, $template);
        $this->info("Vue component created: {$path}");
    }
}
```

By default, Laravel automatically registers all commands within the **app/Console/Commands** directory. So run this command in your terminal:

```sh
php artisan make:vue ComponentName
```

✅ Now, you can enjoy Vue CLI in your code. 😎

Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)