# HTML para Wordpress
## Guia Basico

### 1 - Copiar a pasta do site para wp-content/themes/
Isso vai criar um tema para o wordpress. 
Dica: Usar uma thumbnail para o tema com o nome "screenshot" de 880x660 pixels que deve
ser colocada na raiz do site.

### 2 - Mudar index.html para index.php
Assim o Wordpress localiza o tema.

### 3 - Colocar/criar o arquivo style.css na raiz do tema
O Wordpress apenas vai ler o arquivo se ele estiver na raiz do tema.

### 4 - Adicionar a description do tema
```css
/*
Theme Name: 
Theme URI: 
Author: 
Author URI: 
Description: 
Version: 1.0
*/

```
### 5 - Ativar o tema no Wordpress
Tudo pronto. Basta abrir o Wordpress e trocar o tema.

### 6 - Corrigir o caminho do style.css e outros caminhos se for o caso

```html
link rel="stylesheet" type="text/css" href="<?php echo get_stylesheet_directory_uri(); ?>/style.css">
```

### 7 - Separar o header e o footer em arquivos header.php e footer.php
Uma maneira de tornar o Header e Footer reutilizáveis. Além disso, **deve se adicionar**
```php
<?php wp_head(); ?>
```
antes de fechar a tag **head**. E **deve se adicionar**
```php
<?php wp_footer(); ?>
```
antes de fechar a tag **body**.

Depois disso, basta adicionar
```php
<?php get_header(); ?>
<?php get_footer(); ?>
```
no html para usar o header e o footer.


### 8 - Agora basta substituir o *content* pelas funções php do Wordpress
:)