[com.github.salomonbrys.kodein](../index.md) / [KodeinAwareBase](.)

# KodeinAwareBase

`interface KodeinAwareBase`

Base [KodeinAware](../-kodein-aware.md) interface.

It is separate from [KodeinAware](../-kodein-aware.md) because [Kodein](../-kodein/index.md) implements itself KodeinAwareBase but not [KodeinAware](../-kodein-aware.md).
This is because there are some extension functions to [KodeinAware](../-kodein-aware.md) that would not make sense applied to the [Kodein](../-kodein/index.md) object.
For example, [KodeinAware.withClass](../with-class.md), if applied to [Kodein](../-kodein/index.md), would create a very un-expected result.

### Properties

| Name | Summary |
|---|---|
| [kodein](kodein.md) | `abstract val kodein: `[`Kodein`](../-kodein/index.md)<br>A Kodein Aware class must be within reach of a Kodein object. |

### Extension Properties

| Name | Summary |
|---|---|
| [lazy](../lazy.md) | `val KodeinAwareBase.lazy: `[`LazyKodein`](../-lazy-kodein/index.md)<br>Allows lazy retrieval from a [Kodein](../-kodein/index.md) or [KodeinAware](../-kodein-aware.md) object. |

### Extension Functions

| Name | Summary |
|---|---|
| [With](../-with.md) | `fun <A> KodeinAwareBase.With(argType: `[`TypeToken`](../-type-token/index.md)`<A>, arg: A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>Allows to get a provider or an instance from a curried factory with an `A` argument. |
| [WithF](../-with-f.md) | `fun <A> KodeinAwareBase.WithF(argType: `[`TypeToken`](../-type-token/index.md)`<A>, arg: () -> A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>Allows to get a provider or an instance from a curried factory with an `A` argument. |
| [factory](../factory.md) | `fun <A, T : Any> KodeinAwareBase.factory(tag: Any? = null): (A) -> T`<br>Gets a factory of `T` for the given argument type, return type and tag. |
| [factory](../../com.github.salomonbrys.kodein.erased/factory.md) | `fun <A, T : Any> KodeinAwareBase.factory(tag: Any? = null): (A) -> T`<br>Gets a factory of `T` for the given argument type, return type and tag. |
| [factoryOrNull](../factory-or-null.md) | `fun <A, T : Any> KodeinAwareBase.factoryOrNull(tag: Any? = null): (A) -> T`<br>Gets a factory of `T` for the given argument type, return type and tag, or nul if none is found. |
| [factoryOrNull](../../com.github.salomonbrys.kodein.erased/factory-or-null.md) | `fun <A, T : Any> KodeinAwareBase.factoryOrNull(tag: Any? = null): (A) -> T`<br>Gets a factory of `T` for the given argument type, return type and tag, or nul if none is found. |
| [instance](../instance.md) | `fun <T : Any> KodeinAwareBase.instance(tag: Any? = null): T`<br>Gets an instance of `T` for the given type and tag. |
| [instance](../../com.github.salomonbrys.kodein.erased/instance.md) | `fun <T : Any> KodeinAwareBase.instance(tag: Any? = null): T`<br>Gets an instance of `T` for the given type and tag. |
| [instanceOrNull](../instance-or-null.md) | `fun <T : Any> KodeinAwareBase.instanceOrNull(tag: Any? = null): T?`<br>Gets an instance of `T` for the given type and tag, or null if none is found. |
| [instanceOrNull](../../com.github.salomonbrys.kodein.erased/instance-or-null.md) | `fun <T : Any> KodeinAwareBase.instanceOrNull(tag: Any? = null): T?`<br>Gets an instance of `T` for the given type and tag, or null if none is found. |
| [newInstance](../new-instance.md) | `fun <T> KodeinAwareBase.newInstance(creator: `[`Kodein`](../-kodein/index.md)`.() -> T): T`<br>Allows to create a new instance of an unbound object with the same API as when bounding one. |
| [provider](../provider.md) | `fun <T : Any> KodeinAwareBase.provider(tag: Any? = null): () -> T`<br>Gets a provider of `T` for the given type and tag. |
| [provider](../../com.github.salomonbrys.kodein.erased/provider.md) | `fun <T : Any> KodeinAwareBase.provider(tag: Any? = null): () -> T`<br>Gets a provider of `T` for the given type and tag. |
| [providerOrNull](../provider-or-null.md) | `fun <T : Any> KodeinAwareBase.providerOrNull(tag: Any? = null): () -> T`<br>Gets a provider of `T` for the given type and tag, or null if none is found. |
| [providerOrNull](../../com.github.salomonbrys.kodein.erased/provider-or-null.md) | `fun <T : Any> KodeinAwareBase.providerOrNull(tag: Any? = null): () -> T`<br>Gets a provider of `T` for the given type and tag, or null if none is found. |
| [with](../with.md) | `fun <A> KodeinAwareBase.with(arg: () -> A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>`fun <A> KodeinAwareBase.with(arg: A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>Allows to get a provider or an instance from a curried factory with an `A` argument. |
| [with](../../com.github.salomonbrys.kodein.erased/with.md) | `fun <A> KodeinAwareBase.with(arg: () -> A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>`fun <A> KodeinAwareBase.with(arg: A): `[`CurriedKodeinFactory`](../-curried-kodein-factory/index.md)`<A>`<br>Allows to get a provider or an instance from a curried factory with an `A` argument. |

### Inheritors

| Name | Summary |
|---|---|
| [Kodein](../-kodein/index.md) | `interface Kodein : KodeinAwareBase`<br>KOtlin DEpendency INjection. |
| [KodeinAware](../-kodein-aware.md) | `interface KodeinAware : KodeinAwareBase`<br>Any class that extends this interface can use Kodein "seamlessly". |
