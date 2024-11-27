# Default Nx workspace

I made this repository to demonstrate what a default Nx workspace repositorylooks like.

## Reproduction instructions
1. Create the workspace repository:

    ```sh
    $ pnpm dlx create-nx-workspace --preset=ts
    ```

2. Create first library

    a. Generate library

    ```sh
    $ pnpm nx g @nx/js:lib packages/pkg-a --publishable --importPath=@my-org/pkg-a

    NX  Generating @nx/js:library

    ✔ Which bundler would you like to use to build the library? Choose 'none' to skip build setup. · tsc
    ✔ Which linter would you like to use? · eslint
    ✔ Which unit test runner would you like to use? · vitest
    ```

    b. Commit

    ```sh
    $ git add .
    $ git commit -m 'pkg-a'
    ```

3. Create second library

    a. Generate library

    ```sh
    $ pnpm nx g @nx/js:lib packages/pkg-b --publishable --importPath=@my-org/pkg-b

    NX  Generating @nx/js:library

    ✔ Which bundler would you like to use to build the library? Choose 'none' to skip build setup. · vite
    ✔ Which linter would you like to use? · eslint
    ✔ Which unit test runner would you like to use? · vitest
    ```

    b. Commit

    ```sh
    $ git add .
    $ git commit -m 'pkg-b'
    ```
