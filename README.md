```
# Table of Contents

1.  **$derived**
    *   `$effect.pre`
    *   `$effect.tracking`
    *   `$effect.root`
    *   When not to use `$effect`

2.  **$props**
    *   Fallback values
    *   Renaming props
    *   Rest props
    *   Updating props
    *   Type safety

3.  **$bindable**

4.  **$inspect**
    *   $inspect(...).with
    *   $inspect.trace(...)

5.  **$host**

6.  **Basic markup**
    *   Tags
    *   Element attributes
    *   Component props
    *   Events
        *   Event delegation
    *   Text expressions
    *   Comments

7.  **{#if ...}**

8.  **{#each ...}**
    *   Keyed each blocks
    *   Each blocks without an item
    *   Else blocks

9.  **{#key ...}**

10. **{#await ...}**

11. **{#snippet ...}**
    *   Snippet scope
    *   Passing snippets to components
    *   Typing snippets
    *   Exporting snippets
    *   Programmatic snippets
    *   Snippets and slots

12. **{@render ...}**
    *   Optional snippets

13. **{@html ...}**
    *   Styling

14. **{@const ...}**

15. **{@debug ...}**

16. **bind:**
    *   Function bindings
    *   `<input bind:value>`
    *   `<input bind:checked>`
    *   `<input bind:group>`
    *   `<input bind:files>`
    *   `<select bind:value>`
    *   `<audio>`
    *   `<video>`
    *   `<img>`
    *   `<details bind:open>`
    *   Contenteditable bindings
    *   Dimensions
    *   `bind:this`
    *   `bind:_property_` for components

17. **use:**
    *   Typing

18. **transition:**
    *   Built-in transitions
    *   Local vs global
    *   Transition parameters
    *   Custom transition functions
    *   Transition events

19. **in: and out:**

20. **animate:**
    *   Animation Parameters
    *   Custom animation functions

21. **style:**

22. **class**
    *   Attributes
        *   Objects and arrays
    *   The `class:` directive

23. **Scoped styles**
    *   Specificity
    *   Scoped keyframes

24. **Global styles**
    *   `:global(...)`
    *   `:global`

25. **Custom properties**

26. **Nested `<style>` elements**

27. **`<svelte:boundary>`**
    *   Properties
        *   `failed`
        *   `onerror`

28. **`<svelte:window>`**

29. **`<svelte:document>`**

30. **`<svelte:body>`**

31. **`<svelte:head>`**

32. **`<svelte:element>`**

33. **`<svelte:options>`**

34. **Stores**
    *   When to use stores
    *   svelte/store
        *   `writable`
        *   `readable`
        *   `derived`
        *   `readonly`
        *   `get`
    *   Store contract

35. **Context**
    *   Setting and getting context
    *   Encapsulating context interactions

36. **Lifecycle hooks**
    *   `onMount`
    *   `onDestroy`
    *   `tick`
    *   Deprecated: `beforeUpdate` / `afterUpdate`
        *   Chat window example

37.  **Imperative component API**
    *   `mount`
    *   `unmount`
    *   `render`
    *   `hydrate`

38. **svelte/motion**
    *   Spring
        *   `Spring.of`
    *   Tweened
        *   `Tween.of`

39. **svelte/reactivity/window**
    *   `devicePixelRatio`
    *   `innerHeight`
    *   `innerWidth`
    *   `online`
    *   `outerHeight`
    *   `outerWidth`
    *   `screenLeft`
    *   `screenTop`
    *   `scrollX`
    *   `scrollY`

40. **svelte/reactivity**
    *   `MediaQuery`
    *   `SvelteDate`
    *   `SvelteMap`
    *   `SvelteSet`
    *   `SvelteURL`
        *   `SvelteURLSearchParams`
    *   `createSubscriber`

41. **svelte/server**
    *   `render`

42. **svelte/store**
    *   `derived`
    *   `fromStore`
    *   `get`
    *   `readable`
    *   `readonly`
    *    `toStore`
    *   `writable`
    *   Readable
    *   StartStopNotifier
    *   Subscriber
    *   Unsubscriber
    *   Updater
    *   Writable

43. **svelte/transition**
    *   `blur`
    *   `crossfade`
    *   `draw`
    *   `fade`
    *   `fly`
    *   `scale`
    *   `slide`
    *   BlurParams
    *   CrossfadeParams
    *   DrawParams
    *   EasingFunction
    *   FadeParams
    *   FlyParams
    *   ScaleParams
    *   SlideParams
    *   TransitionConfig

# Start of SvelteKit documentation

1.  **Introduction**
    *   Before we begin
    *   What is SvelteKit?
    *   What is Svelte?
    *   SvelteKit vs Svelte

2.  **Creating a project**
    *   Editor setup

3.  **Project structure**
    *   Project files
        *   `src`
        *   `static`
        *   `tests`
        *   `package.json`
        *   `svelte.config.js`
        *   `tsconfig.json`
        *   `vite.config.js`
    *   Other files
        *   `.svelte-kit`

4.  **Web standards**
    *   Fetch APIs
        *   Request
        *   Response
        *   Headers
    *   FormData
    *   Stream APIs
    *   URL APIs
        *   URLSearchParams
    *   Web Crypto

5.  **Routing**
    *   `+page`
        *   `+page.svelte`
        *   `+page.js`
        *   `+page.server.js`
    *   `+error`
    *   `+layout`
        *   `+layout.svelte`
        *   `+layout.js`
        *   `+layout.server.js`
    *   `+server`
        *   Receiving data
        *   Fallback method handler
        *   Content negotiation
    *   `$types`
    *   Other files
    *   Further reading

6. **Loading data**
    *   Page data
    *   Layout data
    *   Universal vs server
    *   Using URL data
    *   Making fetch requests
    *   Cookies
    *   Headers
    *   Using parent data
    *   Errors
    *   Redirects
    *    Streaming with promises
    *   Parallel loading
    *   Rerunning load functions
    *   Implications for authentication
    *   Further reading

7.  **Form actions**
    *   Default actions
    *   Named actions
    *   Anatomy of an action
        *   Validation errors
        *   Redirects
    *   Loading data
    *   Progressive enhancement
        *   `use:enhance`
        *   Customising `use:enhance`
        *   Custom event listener
    *   Alternatives
    *   GET vs POST
    *   Further reading

8.  **Page options**
    *   `prerender`
        *   Prerendering server routes
        *   When not to prerender
        *   Route conflicts
        *   Troubleshooting
    *   `entries`
    *   `ssr`
    *   `csr`
    *   `trailingSlash`
    *   `config`
    *   Further reading

9.  **State management**
    *   Avoid shared state on the server
    *   Component and page state is preserved
    *   Storing state in the URL
    *   Storing ephemeral state in snapshots

10. **Building your app**
    *   During the build
    *   Preview your app

11. **Adapters**
    *   Using adapters
    *   Platform-specific context

12. **Single-page apps**
    *   Usage
    *   Apache
    *   Prerendering individual pages

13. **Advanced routing**
    *   Rest parameters
        *   404 pages
    *   Optional parameters
    *   Matching
    *   Sorting
    *   Encoding
    *   Advanced layouts
        *   (group)
        *   Breaking out of layouts
        *   +page@
        *   +layout@
        *   When to use layout groups
    *   Further reading

14. **Hooks**
    *   Server hooks
        *   `handle`
        *   `locals`
        *   `handleFetch`
            *   Credentials
    *   Shared hooks
        *   `handleError`
        *   `init`
    *   Universal hooks
        *   `reroute`
        *    `transport`
    *   Further reading

15. **Errors**
    *   Error objects
    *   Expected errors
    *   Unexpected errors
    *   Responses
    *   Type safety
    *   Further reading

16. **Link options**
    *   `data-sveltekit-preload-data`
    *   `data-sveltekit-preload-code`
    *   `data-sveltekit-reload`
    *   `data-sveltekit-replacestate`
    *   `data-sveltekit-keepfocus`
    *   `data-sveltekit-noscroll`
    *   Disabling options

17. **Service workers**
    *   Inside the service worker
    *   During development
    *   Type safety
    *   Other solutions

18. **Server-only modules**
    *   Private environment variables
    *   Server-only utilities
    *   Your modules
    *   How it works
    *   Further reading

19. **Snapshots**

20. **Shallow routing**
    *   API
    *   Loading data for a route
    *   Caveats

21.  **Auth**
    *   Sessions vs tokens
    *   Integration points
    *   Guides

22. **Images**
    *   Vite's built-in handling
    *   `@sveltejs/enhanced-img`
        *   Setup
        *   Basic usage
        *   Dynamically choosing an image
        *   Intrinsic Dimensions
        *   `srcset` and `sizes`
        *   Per-image transforms
    *   Loading images dynamically from a CDN
    *   Best practices

23. **Accessibility**
    *   Route announcements
    *   Focus management
    *   The "lang" attribute
    *   Further reading

24. **SEO**
    *   Out of the box
    *   Manual setup
        *   `<title>` and `<meta>`
        *   Sitemaps
        *   AMP

25. **@sveltejs/kit**
    *   `Server`
    *   `VERSION`
    *   `error`
    *    `fail`
    *   `isActionFailure`
    *   `isHttpError`
    *   `isRedirect`
    *   `json`
    *   `redirect`
    *   `text`
    *   Action
    *   ActionFailure
    *   ActionResult
    *   Actions
    *   Adapter
    *   AfterNavigate
    *   AwaitedActions
    *   BeforeNavigate
    *   Builder
    *   ClientInit
    *   Config
    *   Cookies
    *   Emulator
    *   Handle
    *   HandleClientError
    *   HandleFetch
    *   HandleServerError
    *   HttpError
    *   HttpMethod
    *   Logger
    *   MaybePromise
    *   PrerenderEntryGeneratorMismatchHandler
    *   PrerenderEntryGeneratorMismatchHandlerValue
    *   PrerenderHttpErrorHandler
    *   PrerenderHttpErrorHandlerValue
    *   PrerenderMap
    *   PrerenderMissingIdHandler
    *   PrerenderMissingIdHandlerValue
    *   PrerenderOption
    *   Prerendered
    *   RequestOptions
    *   RouteSegment
    *   TrailingSlash
    *   Csp
        *   CspDirectives

26. **@sveltejs/kit/hooks**
    *   `sequence`

27. **@sveltejs/kit/node/polyfills**
    *   `installPolyfills`

28. **@sveltejs/kit/node**
    *    `createReadableStream`
    *   `getRequest`
    *   `setResponse`

29. **@sveltejs/kit/vite**
    *   `sveltekit`

30. **$app/environment**
    *   `browser`
    *   `building`
    *   `dev`
    *   `version`

31. **$app/forms**
    *   `applyAction`
    *   `deserialize`
    *   `enhance`

32. **$app/navigation**
    *   `afterNavigate`
    *   `beforeNavigate`
    *   `disableScrollHandling`
    *   `goto`
    *   `invalidate`
    *   `invalidateAll`
    *    `onNavigate`
    *   `preloadCode`
    *   `preloadData`
    *   `pushState`
    *   `replaceState`

33. **$app/paths**
    *   `assets`
    *   `base`
    *   `resolveRoute`

34. **$app/server**
    *   `read`

35. **$app/state**
    *   `navigating`
    *   `page`
    *   `updated`

36. **$app/stores**
    *   `getStores`
    *   `navigating`
    *   `page`
    *   `updated`

37. **$env/dynamic/private**

38. **$env/dynamic/public**

39. **$env/static/private**

40. **$env/static/public**

41. **$lib**
    *   `$lib/server`

42. **$service-worker**
    *   `base`
    *   `build`
    *   `files`
    *   `prerendered`
    *   `version`

43. **Configuration**
    *   `compilerOptions`
    *   `extensions`
    *   `kit`
        *   `adapter`
        *   `alias`
        *   `appDir`
        *   `csp`
            *   `mode`
            *   `directives`
            *   `reportOnly`
        *   `csrf`
            *   `checkOrigin`
        *   `embedded`
        *   `env`
            *   `dir`
            *    `publicPrefix`
            *    `privatePrefix`
        *   `files`
            *   `assets`
            *   `hooks`
            *   `lib`
            *   `params`
            *   `routes`
            *   `serviceWorker`
            *   `appTemplate`
            *   `errorTemplate`
        *   `inlineStyleThreshold`
        *    `moduleExtensions`
        *   `outDir`
        *   `output`
            *   `preloadStrategy`
            *   `bundleStrategy`
        *   `paths`
            *    `assets`
            *   `base`
            *   `relative`
        *   `prerender`
            *   `concurrency`
            *   `crawl`
            *   `entries`
            *   `handleHttpError`
            *   `handleMissingId`
            *   `handleEntryGeneratorMismatch`
            *    `origin`
        *   `router`
            *   `type`
        *   `serviceWorker`
            *    `register`
            *   `files?`
        *   `typescript`
            *   `config?`
        *   `version`
            *   `name`
            *   `pollInterval`

44. **Command Line Interface**
    *   `svelte-kit sync`

45. **Types**
    *   Generated types
        *   Default `tsconfig.json`
    *   `$lib`
        *   `$lib/server`
    *    `app.d.ts`
        *   Error
        *   Locals
        *   PageData
        *   PageState
        *   Platform
    *   `Action`
    *   `ActionFailure`
    *   `ActionResult`
    *   `Actions`
    *   `Adapter`
    *   `AfterNavigate`
    *   `AwaitedActions`
    *   `BeforeNavigate`
    *   `Builder`
    *   `ClientInit`
    *   `Config`
    *   `Cookies`
    *   `Emulator`
    *   `Handle`
    *    `HandleClientError`
    *   `HandleFetch`
    *   `HandleServerError`
    *   `HttpError`
    *   `HttpMethod`
    *   `Logger`
    *   `MaybePromise`
    *   `PrerenderEntryGeneratorMismatchHandler`
    *   `PrerenderEntryGeneratorMismatchHandlerValue`
    *   `PrerenderHttpErrorHandler`
    *   `PrerenderHttpErrorHandlerValue`
    *   `PrerenderMap`
    *   `PrerenderMissingIdHandler`
    *   `PrerenderMissingIdHandlerValue`
    *    `PrerenderOption`
    *   `Prerendered`
    *   `RequestOptions`
    *   `RouteSegment`
    *   `TrailingSlash`
    *   `Csp`
        *   `CspDirectives`
    *  `RequestHandler`
    *   `Reroute`
    *   `ResolveOptions`
    *   `RouteDefinition`
    *   `SSRManifest`
    *   `ServerInit`
    *   `ServerInitOptions`
    *    `ServerLoad`
    *   `ServerLoadEvent`
    *   `Snapshot`
    *    `SubmitFunction`
    *    `Transport`
    *   `Transporter`

46. **@sveltejs/kit/hooks**
    *   `sequence`

47. **@sveltejs/kit/node/polyfills**
    *   `installPolyfills`

48. **@sveltejs/kit/node**
    *   `createReadableStream`
    *   `getRequest`
    *   `setResponse`

49. **@sveltejs/kit/vite**
    *    `sveltekit`

50. **$app/environment**
    *   `browser`
    *   `building`
    *   `dev`
    *   `version`

51. **$app/forms**
    *   `applyAction`
    *   `deserialize`
    *    `enhance`

52. **$app/navigation**
    *    `afterNavigate`
    *   `beforeNavigate`
    *   `disableScrollHandling`
    *   `goto`
    *   `invalidate`
    *    `invalidateAll`
    *   `onNavigate`
    *   `preloadCode`
    *   `preloadData`
    *   `pushState`
    *   `replaceState`

53. **$app/paths**
    *   `assets`
    *   `base`
    *   `resolveRoute`

54. **$app/server**
    *   `read`

55. **$app/state**
    *   `navigating`
    *   `page`
    *   `updated`

56. **$app/stores**
    *   `getStores`
    *   `navigating`
    *   `page`
    *   `updated`

57. **$env/dynamic/private**

58. **$env/dynamic/public**

59. **$env/static/private**

60. **$env/static/public**

61. **$lib**

62. **$service-worker**
    *   `base`
    *   `build`
    *   `files`
    *    `prerendered`
    *   `version`

# Start of Svelte CLI documentation

1.  **Overview**
    *   Usage
    *   Acknowledgements

2.  **sv create**
    *   Usage
    *   Options

3.  **sv add**
    *   Usage
    *   Options
    *   Official add-ons

4.  **sv check**
    *   Installation
    *   Usage
    *   Options
    *   Troubleshooting
    *   Machine-readable output
    *   Credits
    *   FAQ

5. **sv migrate**
    *   Usage
    *   Migrations

# Start of Svelte documentation

1.  **Overview**

2.  **Getting started**
    *   Alternatives to SvelteKit
    *   Editor tooling
    *   Getting help

3.  **.svelte files**
    *   `<script>`
    *   `<script module>`
    *   `<style>`

4.  **.svelte.js and .svelte.ts files**

5.  **What are runes?**

6.  **$state**
    *   Deep state
    *   Classes
    *   `$state.raw`
    *   `$state.snapshot`
    *   Passing state into functions

7.  **$derived**
    *   `$derived.by`
    *   Understanding dependencies
    *   Update propagation

8.  **$effect**
    *   Understanding dependencies
    *   `$effect.pre`
    *   `$effect.tracking`
    *   `$effect.root`

9. **Imperative component API**
    *   `mount`
    *   `unmount`
    *   `render`
    *   `hydrate`

10. **Lifecycle hooks**
    *   `onMount`
    *   `onDestroy`
    *   `tick`
    *   Deprecated: `beforeUpdate` / `afterUpdate`
        *   Chat window example

11. **Testing**
    *  Unit and integration testing using Vitest
        *   Using runes inside your test files
        *   Component testing
    *  E2E tests using Playwright

12. **TypeScript**
    *   `<script lang="ts">`
    *   Preprocessor setup
        *   Using SvelteKit or Vite
        *   Other build tools
    *  `tsconfig.json` settings
    *   Typing `$props`
    *   Generic `$props`
    *   Typing wrapper components
    *   Typing `$state`
    *    The `Component` type
    *   Enhancing built-in DOM types

13. **svelte**
    *   `SvelteComponent`
    *   `SvelteComponentTyped`
    *   `afterUpdate`
    *   `beforeUpdate`
    *   `createEventDispatcher`
    *   `createRawSnippet`
    *   `flushSync`
    *   `getAllContexts`
    *   `getContext`
    *    `hasContext`
    *    `hydrate`
    *    `mount`
    *   `onDestroy`
    *    `onMount`
    *   `setContext`
    *   `tick`
    *   `unmount`
    *    `untrack`
    *  `Component`
    *   `ComponentConstructorOptions`
    *   `ComponentEvents`
    *   `ComponentInternals`
    *   `ComponentProps`
    *   `ComponentType`
    *  `EventDispatcher`
    *   `MountOptions`
    *   `Snippet`

14. **svelte/action**
    *   `Action`
    *   `ActionReturn`

15. **svelte/animate**
    *   `flip`
    *   `AnimationConfig`
    *   `FlipParams`

16. **svelte/compiler**
    *    `VERSION`
    *   `compile`
    *   `compileModule`
    *   `migrate`
    *   `parse`
    *   `preprocess`
    *    `walk`
    *   AST
    *   CompileError
    *   CompileOptions
    *   CompileResult
    *   MarkupPreprocessor
    *   ModuleCompileOptions
    *   Preprocessor
    *   PreprocessorGroup
    *   Processed
    *   Warning

17. **svelte/easing**
    *   `backIn`
    *   `backInOut`
    *   `backOut`
    *   `bounceIn`
    *   `bounceInOut`
    *   `bounceOut`
    *   `circIn`
    *   `circInOut`
    *   `circOut`
    *   `cubicIn`
    *   `cubicInOut`
    *   `cubicOut`
    *   `elasticIn`
    *   `elasticInOut`
    *   `elasticOut`
    *   `expoIn`
    *   `expoInOut`
    *   `expoOut`
    *   `linear`
    *   `quadIn`
    *    `quadInOut`
    *   `quadOut`
    *   `quartIn`
    *   `quartInOut`
    *   `quartOut`
    *   `quintIn`
    *    `quintInOut`
    *   `quintOut`
    *   `sineIn`
    *   `sineInOut`
    *   `sineOut`

18. **svelte/events**
    *   `on`

19. **svelte/motion**
    *   `spring`
    *   `tweened`
        * `Spring`
        *   `Spring.of`
        *   `Tween`
        *   `Tween.of`
    * `prefersReducedMotion`

