# Elixir

For å kjøre et program i Elixir, kan du velge mellom tre ulike kommandoer: `iex`, `elixir` og `elixirc`.

## `iex`

IEx er Elixirs interaktive [kommandolinjegrensesnitt](https://hexdocs.pm/iex/1.17.3/IEx.html). Du starter en IEx-økt ved å skrive `iex` i terminalen. I det interaktive miljøet kan du skrive inn et Elixir-uttrykk og få det evaluert umiddelbart:

```elixir
Erlang/OTP 27 [erts-15.0.1] [source] [64-bit] [smp:8:8] [ds:8:8:10] [async-threads:1] [jit]

Interactive Elixir (1.17.3) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> "Hei, Koseprogg!"
"Hei, Koseprogg!"
iex(2)> 84 + 568
652
```

For å avslutte `iex`-økten trykker du `Ctrl+C` to ganger. 

Hvis du vil kjøre en funksjon fra en [modul](https://hexdocs.pm/elixir/1.17.3/modules-and-functions.html) definert i en fil som heter `my_module.ex`, kan du starte IEx med denne filen som argument:

```elixir
iex my_module.ex
```

Deretter kan du kalle funksjoner fra modulen direkte i IEx-økten:

```elixir
Erlang/OTP 27 [erts-15.0.1] [source] [64-bit] [smp:8:8] [ds:8:8:10] [async-threads:1] [jit]

Interactive Elixir (1.17.3) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)> my_module.foo()
...
```

## `elixir`

For å kjøre Elixir-skripter (filer med `.exs`-endelse), kan du bruke `elixir`-kommandoen. Disse filene blir tolket og kjørt direkte uten å bli kompilert først. Skriptet kjøres én gang og avsluttes deretter:

```elixir
elixir my_script.exs
```

## `elixirc`

`elixirc` brukes for å kompilere Elixir-filer (med `.ex`-endelse) til bytekode:

```elixir
elixirc my_module.ex
```

Dette genererer en `.beam`-fil som kan lastes og kjøres i [BEAM](https://en.wikipedia.org/wiki/BEAM_(Erlang_virtual_machine)). Etter kompilering kan du laste inn og bruke modulen i `iex`, forutsatt at du starter `iex` i samme mappe hvor bytekodefilen ligger.