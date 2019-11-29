---
title: "Ejemplo"
description: "Si los valores por defecto son lo suficientemente buenos para tu caso de uso, no tienes que especificarlos para tener un archivo `nuxt.config.js` más corto y limpio."
permalink: /docs/nuxt-optimized-images/example/
created: "2019-03-01T13:35:06.636Z"
published: "2019-03-01T13:35:06.636Z"
modified: "2019-06-05T12:51:34.314Z"
---

# Ejemplo

Las opciones especificadas aquí son los valores **por defecto**. Así que si son lo suficientemente buenos para tu caso de uso, no tienes que especificarlos para así tener un archivo `nuxt.config.js` más corto y limpio.

```javascript
// nuxt.config.js
{
  optimizedImages: {
    inlineImageLimit: 1000,
    imagesName: ({ isDev }) => isDev ? '[path][name][hash:optimized].[ext]' : 'img/[hash:7].[ext]',
    responsiveImagesName: ({ isDev }) => isDev ? '[path][name]--[width][hash:optimized].[ext]' : 'img/[hash:7]-[width].[ext]',
    handleImages: ['jpeg', 'png', 'svg', 'webp', 'gif'],
    optimizeImages: true,
    optimizeImagesInDev: false,
    defaultImageLoader: 'img-loader',
    mozjpeg: {
      quality: 80,
    },
    optipng: {
      optimizationLevel: 3,
    },
    pngquant: false,
    gifsicle: {
      interlaced: true,
      optimizationLevel: 3,
    },
    svgo: {
      // habilitar/deshabilitar plugins svgo aquí
    },
    webp: {
      preset: 'default',
      quality: 75,
    },
  }
}
```
