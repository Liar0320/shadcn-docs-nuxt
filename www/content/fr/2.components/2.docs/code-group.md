---
title: Groupe de Code
icon: lucide:code-xml
badges:
  - value: Nuxt UI Pro
    to: https://ui.nuxt.com/pro/prose/code-group
    target: _blank
  - value: Docus
    to: https://docus.dev/api/components#codegroup
    target: _blank
  - value: Source
    icon: lucide:code
    to: https://github.com/ZTL-UwU/shadcn-docs-nuxt/blob/main/components/content/CodeGroup.vue
    target: _blank
---

## Utilisation

::stack
  ::div{class="p-4"}
    ::code-group
      ```vue [app.vue]
      <template>
        <div>
          <NuxtLayout>
            <NuxtPage />
          </NuxtLayout>
        </div>
      </template>
      ```

      ```vue [pages/index.vue]
      <template>
        <div>
          <h1>Bienvenue sur la page d'accueil</h1>
          <AppAlert>
            Ceci est un composant auto-importé
          </AppAlert>
        </div>
      </template>
      ```
    ::
  ::

  ```mdc
  ::code-group
    ```vue [app.vue]
    <template>
      <div>
        <NuxtLayout>
          <NuxtPage />
        </NuxtLayout>
      </div>
    </template>
    ```

    ```vue [pages/index.vue]
    <template>
      <div>
        <h1>Bienvenue sur la page d'accueil</h1>
        <AppAlert>
          Ceci est un composant auto-importé
        </AppAlert>
      </div>
    </template>
    ```
  ::
  ```
::

::alert{to="/fr/components/docs/tabs"}
`::code-group`{lang="mdc"} est un wrapper autour de `::tabs{variant="card"}`{lang="mdc"}.
::

## Props

:field{name="sync" type="string"}[Portée de synchronisation pour `::tabs`]
