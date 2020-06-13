# Elixir Code Style

## Code for maintainability

Here are [some guidelines](https://ulisses.dev/elixir/2020/02/19/elixir-style-for-maintanability.html) to ensure we write code that's easier to maintain and a joy to work with.

## Documentation

Elixir has first-class support for writing documentation and we should leverage it as much as possible. Below is an example of what we should strive for in our code.

```elixir
@doc """
Creates an app.

## Examples

    iex> create(%{field: value})
    {:ok, %App{}}

    iex> create(%{field: bad_value})
    {:error, %Ecto.Changeset{}}

"""
@spec create(attrs :: Map.t()) :: {:ok, App.t()} | {:error, Ecto.Changeset.t()}
def create(attrs) do
  %App{}
  |> changeset(attrs)
  |> Repo.insert()
end
```

See [Academy.App](https://github.com/mindvalley/platform/blob/master/apps/academy/lib/academy/app/app.ex) as an example of a fully documented module.

## Formatting

Elixir provides a command [mix format](https://hexdocs.pm/mix/master/Mix.Tasks.Format.html) to format file for you.

### When to format code

It is recommended to format code directly in editors, either automatically when saving a file or via an explicit command or key binding.

If you are using VS Code, install [Elixir Formatter](https://marketplace.visualstudio.com/items?itemName=saratravi.elixir-formatter) or [ElixirLS](https://github.com/elixir-lsp/vscode-elixir-ls).

Or, you can run the command manually.

``` bash
cd apps/mindvalley && mix format
```


## A note on Atoms

Erlang/Elixir has a limit on atoms (1,048,576) and they are not garbage collected.

Avoid converting map keys from string to atoms with `String.to_atom/1` especially when the maps data is from external sources like an API payload. This is actually a form of attack. You can use `String.to_existing_atom/1` or cast the payload into a struct, which already have atom keys.

## Naming Convention

*Coming soon...*
