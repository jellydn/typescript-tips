# Typescript Tips [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome 🔥 TypeScript Tips 🔥

If you enjoy TypeScript and really want to use Typesafe, you can check [awesome-typesafe](https://github.com/jellydn/awesome-typesafe)

## 🏠 [Homepage](https://github.com/jellydn/typescript-tips)

### ✨ [Gitbook](https://productsway.gitbook.io/typescript-tips/)

## Contents

- [Tips](#tips)
  - [Matt Pocock](#matt-pocock)
  - [Wes Bos](#wes-bos)
  - [Erik Rasmussen](#erik-rasmussen)
  - [Carlos Caballero](#carlos-caballero)
  - [Ankita Kulkarni](#ankita-kulkarni)
  - [Minko Gechev](#minko-gechev)
  - [Cory House](#cory-house)
  - [Tomek Sułkowski](#tomek-sułkowski)
  - [Sebastien Lorber](#sebastien-lorber)
  - [Steve (Builder.io)](#steve-builderio)
  - [StackBlitz](#stackblitz)
  - [Extending existing types](#extending-existing-types)
  - [Built-in types](#built-in-types)
- [Contribute](#contribute)
  - [Twitter to markdown file](#twitter-to-markdown-file)
- [Credits](#credits)

## Tips

### Matt Pocock

- [TypeScript Tips Series](https://www.totaltypescript.com/tips)
- [Normal union, a discriminated union, and a type predicate](notes/mattpocockuk%20-%201592130978234900484.md)
- [Enter satisfies()() 👀](notes/mattpocockuk%20-%201536670032360611840.md)
- [Use Object.freeze to ensure your objects are readonly at the type level AND the runtime level](notes/mattpocockuk%20-%201542079199543975937.md)
- [Inversion of control](notes/mattpocockuk%20-%201591047557702389760.md)
- [Ultimate TypeScript Thread](notes/mattpocockuk%20-%201509964736275927042.md)
- [Expose type to global with declare global](notes/mattpocockuk%20-%201593584053042630657.md)
- [Use generics to dynamically specify the number, and type, of arguments to functions](notes/mattpocockuk%20-%201509850662795989005.md)
- [Adding things to the global scope in TypeScript](notes/mattpocockuk%20-%201590333383501979649.md)
- [Using 'as const' over enums](notes/mattpocockuk%20-%201598708710523772929.md)
- [Use assertion functions inside classes](notes/mattpocockuk%20-%201512388535692652547.md)

### Wes Bos

- [Four ways to define an object type in TypeScript](notes/wesbos%20-%201524040757518258176.md)
- [The difference between `any` and `unknown`](notes/wesbos%20-%201584905090628034560.md)
- [Use TypeScript's `never` for making sure you hit every scenario](notes/wesbos%20-%201585641232155348992.md)
- [Use TypeScript's `never` to enforce "one or the other" properties on a type](notes/wesbos%20-%201587082842110033926.md)
- [Type Guard in TypeScript by using the `is` keyword in a functions return type](notes/wesbos%20-%201585258976421224450.md)
- [VSCode - quickly add all properties to a typed object in TypeScript with the ts-quickfixes](notes/wesbos%20-%201582803702225989637.md)
- [VSCode - refactoring your codebase](notes/wesbos%20-%201583093975359315968.md)

### Erik Rasmussen

- [Passing around unique identifiers of objects, select the type of the identifier right off of the object type](notes/erikras%20-%201457999235564154882.md)

### Carlos Caballero

- [Use look up tables instead of "if"](notes/Carlillo%20-%201591148366070747347.md)

### Ankita Kulkarni

- [Typescript 4.9 satisfies operator - check if the type matches one of these listed type](notes/kulkarniankita9%20-%201594154991148597250.md)

### Minko Gechev

- [Enum vs const enums](notes/mgechev%20-%201309379618034642946.md)
- [Use labeled tuple elements to get better hints from your text editor ](notes/mgechev%20-%201361186013029269506.md)
- [Use `as const` after literals](notes/mgechev%20-%201462654597059817481.md)

### Cory House

- [Avoid making a property optional when the property isn’t valid in a certain case](notes/housecor%20-%201581638360543600640.md)
- [Alias the type's name when conflicts with an existing identifier](notes/housecor%20-%201586865516395876359.md)
- [Many optional properties are a code smell](notes/housecor%20-%201596861970170671104.md)

### Tomek Sułkowski

- [Extract it from a component using the handy `ComponentProps`](notes/sulco%20-%201160890708615716864.md)
- [Use `keyof` gets a union type of all properties of the given object](notes/sulco%20-%201222507593287028736.md)

### Sebastien Lorber

- [No need to import DOM event handler types](notes/sebastienlorber%20-%201512420374201446405.md)

### Steve (Builder.io)

- [The `satisfies` operator in TypeScript 4.9 is a game changer](notes/Steve8708%20-%201605322303319199744.md)

### StackBlitz

- [Infers array's type as const](notes/stackblitz%20-%201325818478675304448.md)
- [How to use extends](notes/stackblitz%20-%201328353096179789824.md)
- [How to use readonly](notes/stackblitz%20-%201330890655351123968.md)

### Extending existing types

- [`PackageJson`](https://github.com/sindresorhus/type-fest/blob/main/source/package-json.d.ts) - There are a lot of tools that
  place extra configurations inside the `package.json` file. You can extend
  `PackageJson` to support these additional configurations.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://www.typescriptlang.org/play?#code/JYWwDg9gTgLgBDAnmApnA3gBQIYGMDW2A5igFIDOEAdnNuXAEJ0o4HFmVUC+cAZlBBBwA5ElQBaXinIxhAbgCwAKFCRYCZGnQAZYFRgooPfoJHSANntmKlysWlaESFanAC8jZo-YuaAMgwLKwBhal5gIgB+AC44XX1DADpQqnCiLhsgA)

  ```ts
  import type { PackageJson as BasePackageJson } from "type-fest";
  import type { Linter } from "eslint";

  type PackageJson = BasePackageJson & { eslintConfig?: Linter.Config };
  ```

  </details>

### Built-in types

There are many advanced types most users don't know about.

- [`Partial<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#partialtype) -
  Make all properties in `T` optional.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://www.typescriptlang.org/play/#code/JYOwLgpgTgZghgYwgAgHIHsAmEDC6QzADmyA3gLABQyycADnanALYQBcyAzmFKEQNxUaddFDAcQAV2YAjaIMoBfKlQQAbOJ05osEAIIMAQpOBrsUMkOR1eANziRkCfISKSoD4Pg4ZseAsTIALyW1DS0DEysHADkvvoMMQA0VsKi4sgAzAAMuVaKClY2wPaOknSYDrguADwA0sgQAB6QIJjaANYQAJ7oMDp+LsQAfAAUXd0cdUnI9mo+uv6uANp1ALoAlKHhyGAAFsCcAHTOAW4eYF4gyxNrwbNwago0ypRWp66jH8QcAApwYmAjxq8SWIy2FDCNDA3ToKFBQyIdR69wmfQG1TOhShyBgomQX3w3GQE2Q6IA8jIAFYQBBgI4TTiEs5bTQYsFInrLTbbHZOIlgZDlSqQABqj0kKBC3yINx6a2xfOQwH6o2FVXFaklwSCIUkbQghBAEEwENSfNOlykEGefNe5uhB2O6sgS3GPRmLogmslG1tLxUOKgEDA7hAuydtteryAA)

  ```ts
  interface NodeConfig {
    appName: string;
    port: number;
  }

  class NodeAppBuilder {
    private configuration: NodeConfig = {
      appName: "NodeApp",
      port: 3000,
    };

    private updateConfig<Key extends keyof NodeConfig>(
      key: Key,
      value: NodeConfig[Key]
    ) {
      this.configuration[key] = value;
    }

    config(config: Partial<NodeConfig>) {
      type NodeConfigKey = keyof NodeConfig;

      for (const key of Object.keys(config) as NodeConfigKey[]) {
        const updateValue = config[key];

        if (updateValue === undefined) {
          continue;
        }

        this.updateConfig(key, updateValue);
      }

      return this;
    }
  }

  // `Partial<NodeConfig>`` allows us to provide only a part of the
  // NodeConfig interface.
  new NodeAppBuilder().config({ appName: "ToDoApp" });
  ```

  </details>

- [`Required<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#requiredtype) -
  Make all properties in `T` required.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/AQ4SwOwFwUwJwGYEMDGNgGED21VQGJZwC2wA3gFCjXAzFJgA2A-AFzADOUckA5gNxUaIYjA4ckvGG07c+g6gF8KQkAgCuEFFDA5O6gEbEwUbLm2ESwABQIixACJIoSdgCUYAR3Vg4MACYAPGYuFvYAfACU5Ko0APRxwADKMBD+wFAAFuh2Vv7OSBlYGdmc8ABu8LHKsRyGxqY4oQT21pTCIHQMjOwA5DAAHgACxAAOjDAAdChYxL0ANLHUouKSMH0AEmAAhJhY6ozpAJ77GTCMjMCiV0ToSAb7UJPPC9WRgrEJwAAqR6MwSRQPFGUFocDgRHYxnEfGAowh-zgUCOwF6KwkUl6tXqJhCeEsxDaS1AXSYfUGI3GUxmc0WSneQA)

  ```ts
  interface ContactForm {
    email?: string;
    message?: string;
  }

  function submitContactForm(formData: Required<ContactForm>) {
    // Send the form data to the server.
  }

  submitContactForm({
    email: "ex@mple.com",
    message: "Hi! Could you tell me more about�",
  });

  // TypeScript error: missing property 'message'
  submitContactForm({
    email: "ex@mple.com",
  });
  ```

  </details>

- [`Readonly<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#readonlytype) -
  Make all properties in `T` readonly.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/AQ4UwOwVwW2AZA9gc3mAbmANsA3gKFCOAHkAzMgGkOJABEwAjKZa2kAUQCcvEu32AMQCGAF2FYBIAL4BufDRABLCKLBcywgMZgEKZOoDCiCGSXI8i4hGEwwALmABnUVxXJ57YFgzZHSVF8sT1BpBSItLGEnJz1kAy5LLy0TM2RHACUwYQATEywATwAeAITjU3MAPnkrCJMXLigtUT4AClxgGztKbyDgaX99I1TzAEokr1BRAAslJwA6FIqLAF48TtswHp9MHDla9hJGACswZvmyLjAwAC8wVpm5xZHkUZDaMKIwqyWXYCW0oN4sNlsA1h0ug5gAByACyBQAggAHJHQ7ZBIFoXbzBjMCz7OoQP5YIaJNYQMAAdziCVaALGNSIAHomcAACoFJFgADKWjcSNEwG4vC4ji0wggEEQguiTnMEGALWAV1yAFp8gVgEjeFyuKICvMrCTgVxnst5jtsGC4ljsPNhXxGaAWcAAOq6YRXYDCRg+RWIcA5JSC+kWdCepQ+v3RYCU3RInzRMCGwlpC19NYBW1Ye08R1AA)

  ```ts
  enum LogLevel {
    Off,
    Debug,
    Error,
    Fatal,
  }

  interface LoggerConfig {
    name: string;
    level: LogLevel;
  }

  class Logger {
    config: Readonly<LoggerConfig>;

    constructor({ name, level }: LoggerConfig) {
      this.config = { name, level };
      Object.freeze(this.config);
    }
  }

  const config: LoggerConfig = {
    name: "MyApp",
    level: LogLevel.Debug,
  };

  const logger = new Logger(config);

  // TypeScript Error: cannot assign to read-only property.
  logger.config.level = LogLevel.Error;

  // We are able to edit config variable as we please.
  config.level = LogLevel.Error;
  ```

  </details>

- [`Pick<T, K>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#picktype-keys) -
  From `T`, pick a set of properties whose keys are in the union `K`.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/AQ4SwOwFwUwJwGYEMDGNgEE5TCgNugN4BQoZwOUBAXMAM5RyQDmA3KeSFABYCuAtgCMISMHloMmENh04oA9tBjQJjFuzIBfYrOAB6PcADCcGElh1gEGAHcKATwAO6ebyjB5CTNlwFwSxFR0BX5HeToYABNgBDh5fm8cfBg6AHIKG3ldA2BHOOcfFNpUygJ0pAhokr4hETFUgDpswywkggAFUwA3MFtgAF5gQgowKhhVKTYKGuFRcXo1aVZgbTIoJ3RW3xhOmB6+wfbcAGsAHi3kgBpgEtGy4AAfG54BWfqAPnZm4AAlZUj4MAkMA8GAGB4vEgfMlLLw6CwPBA8PYRmMgZVgAC6CgmI4cIommQELwICh8RBgKZKvALh1ur0bHQABR5PYMui0Wk7em2ADaAF0AJS0AASABUALIAGQAogR+Mp3CROCAFBBwVC2ikBpj5CgBIqGjizLA5TAFdAmalImAuqlBRoVQh5HBgEy1eDWfs7J5cjzGYKhroVfpDEhHM4MV6GRR5NN0JrtnRg6BVirTFBeHAKYmYY6QNpdB73LmCJZBlSAXAubtvczeSmQMNSuMbmKNgBlHFgPEUNwusBIPAAQlS1xetTmxT0SDoESgdD0C4aACtHMwxytLrohawgA)

  ```ts
  interface Article {
    title: string;
    thumbnail: string;
    content: string;
  }

  // Creates new type out of the `Article` interface composed
  // from the Articles' two properties: `title` and `thumbnail`.
  // `ArticlePreview = {title: string; thumbnail: string}`
  type ArticlePreview = Pick<Article, "title" | "thumbnail">;

  // Render a list of articles using only title and description.
  function renderArticlePreviews(previews: ArticlePreview[]): HTMLElement {
    const articles = document.createElement("div");

    for (const preview of previews) {
      // Append preview to the articles.
    }

    return articles;
  }

  const articles = renderArticlePreviews([
    {
      title: "TypeScript tutorial!",
      thumbnail: "/assets/ts.jpg",
    },
  ]);
  ```

  </details>

- [`Record<K, T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#recordkeys-type) -
  Construct a type with a set of properties `K` of type `T`.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/AQ4ejYAUHsGcCWAXBMB2dgwGbAKYC2ADgDYwCeeemCaWArgE7ADGMxAhmuQHQBQoYEnJE8wALKEARnkaxEKdMAC8wAOS0kstGuAAfdQBM8ANzxlRjXQbVaWACwC0JPB0NqA3HwGgIwAJJoWozYHCxixnAsjAhStADmwESMMJYo1Fi4HMCIaPEu+MRklHj8gpqyoeHAAKJFFFTAAN4+giDYCIxwSAByHAR4AFw5SDF5Xm2gJBzdfQPD3WPxE5PAlBxdAPLYNQAelgh4aOHDaPQEMowrIAC+3oJ+AMKMrlrAXFhSAFZ4LEhC9g4-0BmA4JBISXgiCkBQABpILrJ5MhUGhYcATGD6Bk4Hh-jNgABrPDkOBlXyQAAq9ngYmJpOAAHcEOCRjAXqwYODfoo6DhakUSph+Uh7GI4P0xER4Cj0OSQGwMP8tP1hgAlX7swwAHgRl2RvIANALSA08ABtAC6AD4VM1Wm0Kow0MMrYaHYJjGYLLJXZb3at1HYnC43Go-QHQDcvA6-JsmEJXARgCDgMYWAhjIYhDAU+YiMAAFIwex0ZmilMITCGF79TLAGRsAgJYAAZRwSEZGzEABFTOZUrJ5Yn+jwnWgeER6HB7AAKJrADpdXqS4ZqYultTG6azVfqHswPBbtauLY7fayQ7HIbAAAMwBuAEoYw9IBq2Ixs9h2eFMOQYPQObALQKJgggABeYhghCIpikkKRpOQRIknAsZUiIeCttECBEP8NSMCkjDDAARMGziuIYxHwYOjDCMBmDNnAuTxA6irdCOBB1Lh5Dqpqn66tISIykawBnOCtqqC0gbjqc9DgpGkxegOliyfJDrRkAA)

  ```ts
  // Positions of employees in our company.
  type MemberPosition = "intern" | "developer" | "tech-lead";

  // Interface describing properties of a single employee.
  interface Employee {
    firstName: string;
    lastName: string;
    yearsOfExperience: number;
  }

  // Create an object that has all possible `MemberPosition` values set as keys.
  // Those keys will store a collection of Employees of the same position.
  const team: Record<MemberPosition, Employee[]> = {
    intern: [],
    developer: [],
    "tech-lead": [],
  };

  // Our team has decided to help John with his dream of becoming Software Developer.
  team.intern.push({
    firstName: "John",
    lastName: "Doe",
    yearsOfExperience: 0,
  });

  // `Record` forces you to initialize all of the property keys.
  // TypeScript Error: "tech-lead" property is missing
  const teamEmpty: Record<MemberPosition, null> = {
    intern: null,
    developer: null,
  };
  ```

  </details>

- [`Exclude<T, U>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#excludetype-excludedunion) -
  Exclude from `T` those types that are assignable to `U`.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/JYOwLgpgTgZghgYwgAgMrQG7QMIHsQzADmyA3gFDLIAOuUYAXMiAK4A2byAPsgM5hRQJHqwC2AI2gBucgF9y5MAE9qKAEoQAjiwj8AEnBAATNtGQBeZAAooWphu26wAGmS3e93bRC8IASgsAPmRDJRlyAHoI5ABRAA8ENhYjFFYOZGVVZBgoXFFkAAM0zh5+QRBhZhYJaAKAOkjogEkQZAQ4X2QAdwALCFbaemRgXmQtFjhOMFwq9K6ULuB0lk6U+HYwZAxJnQaYFhAEMGB8ZCIIMAAFOjAANR2IK0HGWISklIAedCgsKDwCYgAbQA5M9gQBdVzFQJ+JhiSRQMiUYYwayZCC4VHPCzmSzAspCYEBWxgFhQAZwKC+FpgJ43VwARgADH4ZFQSWSBjcZPJyPtDsdTvxKWBvr8rD1DCZoJ5HPopaYoK4EPhCEQmGKcKriLCtrhgEYkVQVT5Nr4fmZLLZtMBbFZgT0wGBqES6ghbHBIJqoBKFdBWQpjfh+DQbhY2tqiHVsbjLMVkAB+ZAAZiZaeQTHOVxu9ySjxNaujNwDVHNvzqbBGkBAdPoAfkQA)

  ```ts
  interface ServerConfig {
    port: null | string | number;
  }

  type RequestHandler = (request: Request, response: Response) => void;

  // Exclude `null` type from `null | string | number`.
  // In case the port is equal to `null`, we will use default value.
  function getPortValue(port: Exclude<ServerConfig["port"], null>): number {
    if (typeof port === "string") {
      return parseInt(port, 10);
    }

    return port;
  }

  function startServer(handler: RequestHandler, config: ServerConfig): void {
    const server = require("http").createServer(handler);

    const port = config.port === null ? 3000 : getPortValue(config.port);
    server.listen(port);
  }
  ```

  </details>

- [`Extract<T, U>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#extracttype-union) -
  Extract from `T` those types that are assignable to `U`.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/CYUwxgNghgTiAEAzArgOzAFwJYHtXzSwEdkQBJYACgEoAueVZAWwCMQYBuAKDDwGcM8MgBF4AXngBlAJ6scESgHIRi6ty5ZUGdoihgEABXZ888AN5d48ANoiAuvUat23K6ihMQ9ATE0BzV3goPy8GZjZOLgBfLi4Aejj4AEEICBwAdz54MAALKFQQ+BxEeAAHY1NgKAwoIKy0grr4DByEUpgccpgMaXgAaxBerCzi+B9-ZulygDouFHRsU1z8kKMYE1RhaqgAHkt4AHkWACt4EAAPbVRgLLWNgBp9gGlBs8uQa6yAUUuYPQwdgNpKM7nh7mMML4CgA+R5WABqUAgpDeVxuhxO1he0jsXGh8EoOBO9COx3BQPo2PBADckaR6IjkSA6PBqTgsMBzPsicdrEC7OJWXSQNwYvFEgAVTS9JLXODpeDpKBZFg4GCoWa8VACIJykAKiQWKy2YQOAioYikCg0OEMDyhRSy4DyxS24KhAAMjyi6gS8AAwjh5OD0iBFHAkJoEOksC1mnkMJq8gUQKDNttKPlnfrwYp3J5XfBHXqoKpfYkAOI4ansTxaeDADmoRSCCBYAbxhC6TDx6rwYHIRX5bScjA4bLJwoDmDwDkfbA9JMrVMVdM1TN69LgkTgwgkchUahqIA)

  ```ts
  declare function uniqueId(): number;

  const ID = Symbol("ID");

  interface Person {
    [ID]: number;
    name: string;
    age: number;
  }

  // Allows changing the person data as long as the property key is of string type.
  function changePersonData<
    Obj extends Person,
    Key extends Extract<keyof Person, string>,
    Value extends Obj[Key]
  >(obj: Obj, key: Key, value: Value): void {
    obj[key] = value;
  }

  // Tiny Andrew was born.
  const andrew = {
    [ID]: uniqueId(),
    name: "Andrew",
    age: 0,
  };

  // Cool, we're fine with that.
  changePersonData(andrew, "name", "Pony");

  // Goverment didn't like the fact that you wanted to change your identity.
  changePersonData(andrew, ID, uniqueId());
  ```

  </details>

- [`NonNullable<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#nonnullabletype) -
  Exclude `null` and `undefined` from `T`.
  <details>
  <summary>
  		Example
  </summary>
  Works with <a href="https://www.typescriptlang.org/tsconfig#strictNullChecks"><code>strictNullChecks</code></a> set to <code>true</code>.

  [Playground](https://typescript-play.js.org/?target=6#code/C4TwDgpgBACg9gJ2AOQK4FsBGEFQLxQDOwCAlgHYDmUAPlORtrnQwDasDcAUFwPQBU-WAEMkUOADMowqAGNWwwoSgATCBIqlgpOOSjAAFsOBRSy1IQgr9cKJlSlW1mZYQA3HFH68u8xcoBlHA8EACEHJ08Aby4oKDBUTFZSWXjEFEYcAEIALihkXTR2YSSIAB54JDQsHAA+blj4xOTUsHSACkMzPKD3HHDHNQQAGjSkPMqMmoQASh7g-oihqBi4uNIpdraxPAI2VhmVxrX9AzMAOm2ppnwoAA4ABifuE4BfKAhWSyOTuK7CS7pao3AhXF5rV48E4ICDAVAIPT-cGQyG+XTEIgLMJLTx7CAAdygvRCA0iCHaMwarhJOIQjUBSHaACJHk8mYdeLwxtdcVAAOSsh58+lXdr7Dlcq7A3n3J4PEUdADMcspUE53OluAIUGVTx46oAKuAIAFZGQwCYAKIIBCILjUxaDHAMnla+iodjcIA)

  ```ts
  type PortNumber = string | number | null;

  /** Part of a class definition that is used to build a server */
  class ServerBuilder {
    portNumber!: NonNullable<PortNumber>;

    port(this: ServerBuilder, port: PortNumber): ServerBuilder {
      if (port == null) {
        this.portNumber = 8000;
      } else {
        this.portNumber = port;
      }

      return this;
    }
  }

  const serverBuilder = new ServerBuilder();

  serverBuilder
    .port("8000") // portNumber = '8000'
    .port(null) // portNumber =  8000
    .port(3000); // portNumber =  3000

  // TypeScript error
  serverBuilder.portNumber = null;
  ```

  </details>

- [`Parameters<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#parameterstype) -
  Obtain the parameters of a function type in a tuple.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/GYVwdgxgLglg9mABAZwBYmMANgUwBQxgAOIUAXIgIZgCeA2gLoCUFAbnDACaIDeAUIkQB6IYgCypSlBxUATrMo1ECsJzgBbLEoipqAc0J7EMKMgDkiHLnU4wp46pwAPHMgB0fAL58+oSLARECEosLAA5ABUYG2QAHgAxJGdpVWREPDdMylk9ZApqemZEAF4APipacrw-CApEgBogkKwAYThwckQwEHUAIxxZJl4BYVEImiIZKF0oZRwiWVdbeygJmThgOYgcGFYcbhqApCJsyhtpWXcR1cnEePBoeDAABVPzgbTixFeFd8uEsClADcIxGiygIFkSEOT3SmTc2VydQeRx+ZxwF2QQ34gkEwDgsnSuFmMBKiAADEDjIhYk1Qm0OlSYABqZnYka4xA1DJZHJYkGc7yCbyeRA+CAIZCzNAYbA4CIAdxg2zJwVCkWirjwMswuEaACYmCCgA)

  ```ts
  function shuffle(input: any[]): void {
    // Mutate array randomly changing its' elements indexes.
  }

  function callNTimes<Fn extends (...args: any[]) => any>(
    func: Fn,
    callCount: number
  ) {
    // Type that represents the type of the received function parameters.
    type FunctionParameters = Parameters<Fn>;

    return function (...args: FunctionParameters) {
      for (let i = 0; i < callCount; i++) {
        func(...args);
      }
    };
  }

  const shuffleTwice = callNTimes(shuffle, 2);
  ```

  </details>

- [`ConstructorParameters<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#constructorparameterstype) -
  Obtain the parameters of a constructor function type in a tuple.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/MYGwhgzhAECCBOAXAlqApgWQPYBM0mgG8AoaaFRENALmgkXmQDsBzAblOmCycTV4D8teo1YdO3JiICuwRFngAKClWENmLAJRFOZRAAtkEAHQq00ALzlklNBzIBfYk+KhIMAJJTEYJsDQAwmDA+mgAPAAq0GgAHnxMODCKTGgA7tCKxllg8CwQtL4AngDaALraFgB80EWa1SRkAA6MAG5gfNAB4FABPDJyCrQR9tDNyG0dwMGhtBhgjWEiGgA00F70vv4RhY3hEZXVVinpc42KmuJkkv3y8Bly8EPaDWTkhiZd7r3e8LK3llwGCMXGQWGhEOsfH5zJlsrl8p0+gw-goAAo5MAAW3BaHgEEilU0tEhmzQ212BJ0ry4SOg+kg+gBBiMximIGA0nAfAQLGk2N4EAAEgzYcYcnkLsRdDTvNEYkYUKwSdCme9WdM0MYwYhFPSIPpJdTkAAzDKxBUaZX+aAAQgsVmkCTQxuYaBw2ng4Ok8CYcotSu8pMur09iG9vuObxZnx6SN+AyUWTF8MN0CcZE4Ywm5jZHK5aB5fP4iCFIqT4oRRTKRLo6lYVNeAHpG50wOzOe1zHr9NLQ+HoABybsD4HOKXXRA1JCoKhBELmI5pNaB6Fz0KKBAodDYPAgSUTmqYsAALx4m5nC6nW9nGq14KtaEUA9gR9PvuNCjQ9BgACNvcwNBtAcLiAA)

  ```ts
  class ArticleModel {
    title: string;
    content?: string;

    constructor(title: string) {
      this.title = title;
    }
  }

  class InstanceCache<T extends new (...args: any[]) => any> {
    private ClassConstructor: T;
    private cache: Map<string, InstanceType<T>> = new Map();

    constructor(ctr: T) {
      this.ClassConstructor = ctr;
    }

    getInstance(...args: ConstructorParameters<T>): InstanceType<T> {
      const hash = this.calculateArgumentsHash(...args);

      const existingInstance = this.cache.get(hash);
      if (existingInstance !== undefined) {
        return existingInstance;
      }

      return new this.ClassConstructor(...args);
    }

    private calculateArgumentsHash(...args: any[]): string {
      // Calculate hash.
      return "hash";
    }
  }

  const articleCache = new InstanceCache(ArticleModel);
  const amazonArticle = articleCache.getInstance("Amazon forests burining!");
  ```

  </details>

- [`ReturnType<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#returntypetype) -
  Obtain the return type of a function type.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/MYGwhgzhAECSAmICmBlJAnAbgS2E6A3gFDTTwD2AcuQC4AW2AdgOYAUAlAFzSbnbyEAvkWFFQkGJSQB3GMVI1sNZNwg10TZgG4S0YOUY0kh1es07d+xmvQBXYDXLpWi5UlMaWAGj0GjJ6BtNdkJdBQYIADpXZGgAXmgYpB1ScOwoq38aeN9DYxoU6GFRKzVoJjUwRjwAYXJbPPRuAFkwAAcAHgAxBodsAx9GWwBbACMMAD4cxhloVraOCyYjdAAzMDxoOut1e0d0UNIZ6WhWSPOwdGYIbiqATwBtAF0uaHudUQB6ACpv6ABpJBINqJdAbADW0Do5BOw3u5R2VTwMHIq2gAANtjZ0bkbHsnFCwJh8ONjHp0EgwEZ4JFoN9PkRVr1FAZoMwkDRYIjqkgOrosepoEgAB7+eAwAV2BxOLy6ACCVxgIrFEoMeOl6AACpcwMMORgIB1JRMiBNWKVdhruJKfOdIpdrtwFddXlzKjyACp3Nq842HaDIbL6BrZBIVGhIpB1EMYSLsmjmtWW-YhAA+qegAAYLKQLQj3ZsEsdccmnGcLor2Dn8xGedHGpEIBzEzspfsfMHDNAANTQACMVaIljV5GQkRA5DYmIpVKQAgAJARO9le33BDXIyi0YuLW2nJFGLqkOvxFB0YPdBSaLZ0IwNzyPkO8-xkGgsLh8Al427a3hWAhXwwHA8EHT5PmgAB1bAQBAANJ24adKWpft72RaBUTgRBUCAj89HAM8xCTaBjggABRQx0DuHJv25P9dCkWRZVIAAiBjoFImpmjlFBgA0NpsjadByDacgIDAEAIAAQmYpjoGYgAZSBsmGPw6DtZiiFA8CoJguDmAQmoZ2QvtUKQLdoAYmBTwgdEiCAA)

  ```ts
  /** Provides every element of the iterable `iter` into the `callback` function and stores the results in an array. */
  function mapIter<
    Elem,
    Func extends (elem: Elem) => any,
    Ret extends ReturnType<Func>
  >(iter: Iterable<Elem>, callback: Func): Ret[] {
    const mapped: Ret[] = [];

    for (const elem of iter) {
      mapped.push(callback(elem));
    }

    return mapped;
  }

  const setObject: Set<string> = new Set();
  const mapObject: Map<number, string> = new Map();

  mapIter(setObject, (value: string) => value.indexOf("Foo")); // number[]

  mapIter(mapObject, ([key, value]: [number, string]) => {
    return key % 2 === 0 ? value : "Odd";
  }); // string[]
  ```

  </details>

- [`InstanceType<T>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#instancetypetype) -
  Obtain the instance type of a constructor function type.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/MYGwhgzhAECSAmICmBlJAnAbgS2E6A3gFDTTwD2AcuQC4AW2AdgOYAUAlAFzSbnbyEAvkWFFQkGJSQB3GMVI1sNZNwg10TZgG4S0YOUY0kh1es07d+xmvQBXYDXLpWi5UlMaWAGj0GjJ6BtNdkJdBQYIADpXZGgAXmgYpB1ScOwoq38aeN9DYxoU6GFRKzVoJjUwRjwAYXJbPPRuAFkwAAcAHgAxBodsAx9GWwBbACMMAD4cxhloVraOCyYjdAAzMDxoOut1e0d0UNIZ6WhWSPOwdGYIbiqATwBtAF0uaHudUQB6ACpv6ABpJBINqJdAbADW0Do5BOw3u5R2VTwMHIq2gAANtjZ0bkbHsnFCwJh8ONjHp0EgwEZ4JFoN9PkRVr1FAZoMwkDRYIjqkgOrosepoEgAB7+eAwAV2BxOLy6ACCVxgIrFEoMeOl6AACpcwMMORgIB1JRMiBNWKVdhruJKfOdIpdrtwFddXlzKjyACp3Nq842HaDIbL6BrZBIVGhIpB1EMYSLsmjmtWW-YhAA+qegAAYLKQLQj3ZsEsdccmnGcLor2Dn8xGedHGpEIBzEzspfsfMHDNAANTQACMVaIljV5GQkRA5DYmIpVKQAgAJARO9le33BDXIyi0YuLW2nJFGLqkOvxFB0YPdBSaLZ0IwNzyPkO8-xkGgsLh8Al427a3hWAhXwwHA8EHT5PmgAB1bAQBAANJ24adKWpft72RaBUTgRBUCAj89HAM8xCTaBjggABRQx0DuHJv25P9dCkWRZVIAAiBjoFImpmjlFBgA0NpsjadByDacgIDAEAIAAQmYpjoGYgAZSBsmGPw6DtZiiFA8CoJguDmAQmoZ2QvtUKQLdoAYmBTwgdEiCAA)

  ```ts
  class IdleService {
    doNothing(): void {}
  }

  class News {
    title: string;
    content: string;

    constructor(title: string, content: string) {
      this.title = title;
      this.content = content;
    }
  }

  const instanceCounter: Map<Function, number> = new Map();

  interface Constructor {
    new (...args: any[]): any;
  }

  // Keep track how many instances of `Constr` constructor have been created.
  function getInstance<
    Constr extends Constructor,
    Args extends ConstructorParameters<Constr>
  >(constructor: Constr, ...args: Args): InstanceType<Constr> {
    let count = instanceCounter.get(constructor) || 0;

    const instance = new constructor(...args);

    instanceCounter.set(constructor, count + 1);

    console.log(`Created ${count + 1} instances of ${Constr.name} class`);

    return instance;
  }

  const idleService = getInstance(IdleService);
  // Will log: `Created 1 instances of IdleService class`
  const newsEntry = getInstance(
    News,
    "New ECMAScript proposals!",
    "Last month..."
  );
  // Will log: `Created 1 instances of News class`
  ```

  </details>

- [`Omit<T, K>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#omittype-keys) -
  Constructs a type by picking all properties from T and then removing K.
  <details>
  <summary>
  		Example
  </summary>

  [Playground](https://typescript-play.js.org/?target=6#code/JYOwLgpgTgZghgYwgAgIImAWzgG2QbwChlks4BzCAVShwC5kBnMKUcgbmKYAcIFgIjBs1YgOXMpSFMWbANoBdTiW5woFddwAW0kfKWEAvoUIB6U8gDCUCHEiNkICAHdkYAJ69kz4GC3JcPG4oAHteKDABBxCYNAxsPFBIWEQUCAAPJG4wZABySUFcgJAAEzMLXNV1ck0dIuCw6EjBADpy5AB1FAQ4EGQAV0YUP2AHDy8wEOQbUugmBLwtEIA3OcmQnEjuZBgQqE7gAGtgZAhwKHdkHFGwNvGUdDIcAGUliIBJEF3kAF5kAHlML4ADyPBIAGjyBUYRQAPnkqho4NoYQA+TiEGD9EAISIhPozErQMG4AASK2gn2+AApek9pCSXm8wFSQooAJQMUkAFQAsgAZACiOAgmDOOSIJAQ+OYyGl4DgoDmf2QJRCCH6YvALQQNjsEGFovF1NyJWAy1y7OUyHMyE+yRAuFImG4Iq1YDswHxbRINjA-SgfXlHqVUE4xiAA)

  ```ts
  interface Animal {
    imageUrl: string;
    species: string;
    images: string[];
    paragraphs: string[];
  }

  // Creates new type with all properties of the `Animal` interface
  // except 'images' and 'paragraphs' properties. We can use this
  // type to render small hover tooltip for a wiki entry list.
  type AnimalShortInfo = Omit<Animal, "images" | "paragraphs">;

  function renderAnimalHoverInfo(animals: AnimalShortInfo[]): HTMLElement {
    const container = document.createElement("div");
    // Internal implementation.
    return container;
  }
  ```

  </details>

- [`Uppercase<S extends string>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#uppercasestringtype) -
  Transforms every character in a string into uppercase.
  <details>
  <summary>
  	Example
  </summary>

  ```ts
  type T = Uppercase<"hello">; // 'HELLO'

  type T2 = Uppercase<"foo" | "bar">; // 'FOO' | 'BAR'

  type T3<S extends string> = Uppercase<`aB${S}`>;
  type T4 = T3<"xYz">; // 'ABXYZ'

  type T5 = Uppercase<string>; // string
  type T6 = Uppercase<any>; // any
  type T7 = Uppercase<never>; // never
  type T8 = Uppercase<42>; // Error, type 'number' does not satisfy the constraint 'string'
  ```

  </details>

- [`Lowercase<S extends string>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#lowercasestringtype) -
  Transforms every character in a string into lowercase.
  <details>
  <summary>
  	Example
  </summary>

  ```ts
  type T = Lowercase<"HELLO">; // 'hello'

  type T2 = Lowercase<"FOO" | "BAR">; // 'foo' | 'bar'

  type T3<S extends string> = Lowercase<`aB${S}`>;
  type T4 = T3<"xYz">; // 'abxyz'

  type T5 = Lowercase<string>; // string
  type T6 = Lowercase<any>; // any
  type T7 = Lowercase<never>; // never
  type T8 = Lowercase<42>; // Error, type 'number' does not satisfy the constraint 'string'
  ```

  </details>

- [`Capitalize<S extends string>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#capitalizestringtype) -
  Transforms the first character in a string into uppercase.
  <details>
  <summary>
  	Example
  </summary>

  ```ts
  type T = Capitalize<"hello">; // 'Hello'

  type T2 = Capitalize<"foo" | "bar">; // 'Foo' | 'Bar'

  type T3<S extends string> = Capitalize<`aB${S}`>;
  type T4 = T3<"xYz">; // 'ABxYz'

  type T5 = Capitalize<string>; // string
  type T6 = Capitalize<any>; // any
  type T7 = Capitalize<never>; // never
  type T8 = Capitalize<42>; // Error, type 'number' does not satisfy the constraint 'string'
  ```

  </details>

- [`Uncapitalize<S extends string>`](https://www.typescriptlang.org/docs/handbook/utility-types.html#uncapitalizestringtype) -
  Transforms the first character in a string into lowercase.
  <details>
  <summary>
  	Example
  </summary>

  ```ts
  type T = Uncapitalize<"Hello">; // 'hello'

  type T2 = Uncapitalize<"Foo" | "Bar">; // 'foo' | 'bar'

  type T3<S extends string> = Uncapitalize<`AB${S}`>;
  type T4 = T3<"xYz">; // 'aBxYz'

  type T5 = Uncapitalize<string>; // string
  type T6 = Uncapitalize<any>; // any
  type T7 = Uncapitalize<never>; // never
  type T8 = Uncapitalize<42>; // Error, type 'number' does not satisfy the constraint 'string'
  ```

  </details>

You can find some examples in the
[TypeScript docs](https://www.typescriptlang.org/docs/handbook/utility-types.html).

## Contribute

Contributions welcome! Read the [contribution guidelines](docs/contributing.md)
first.

### Twitter to markdown file

Create .envrc and fill the value then Use [tweet-to-markdown](https://github.com/kbravh/tweet-to-markdown)

```sh
# .envrc
export TTM_API_KEY=YOUR_API_KEY
```

Then run the [direnv](https://direnv.net/) command

```sh
 direnv allow .
```

And, generate markdown from a twitter url

```sh
npx tweet-to-markdown -p notes https://twitter.com/mattpocockuk/status/1509964736275927042\?s\=20\&t\=sA-g5MNM5TPjN6Ozs1qxgA
```

Then save video if available

```sh
npx twt-dl-cli@latest https://twitter.com/mattpocockuk/status/1592130978234900484
```

Finally, add the [Thread Reader App](https://threadreaderapp.com) at the end with below format.

```markdown
[Thread by @USERNAME on Thread Reader App](https://threadreaderapp.com/thread/STATUS_ID.html)
```

NOTE: I have sent a pull request about this step to `tweet-to-markdown` repository: [feat: add Thread Reader App link and the end #19](https://github.com/kbravh/tweet-to-markdown/pull/19) Might not need this step if this PR is accepted.

## Credits

This project is made by community and especially the wonderful people and projects listed in this document

### Open Source

- [sindresorhus/type-fest](https://github.com/sindresorhus/type-fest): for 2 sections (Extending existing type, Built-in types)
- [kbravh/tweet-to-markdown](https://github.com/kbravh/tweet-to-markdown): A command line tool to convert Tweets to Markdown.
- [Thread Reader App](https://threadreaderapp.com/): Thread Reader helps you read and share Twitter threads easily!
- [egoist/download-twitter-video](https://github.com/egoist/download-twitter-video) : The easiest way to download any Twitter video

### Tech Twitter

- [Matt Pocock ✈️ Modern Frontends](https://twitter.com/mattpocockuk)
- [Wes Bos](https://twitter.com/wesbos)
- [Erik Rasmussen](https://twitter.com/erikras)
- [Carlos Caballero](https://twitter.com/Carlillo)
- [Ankita Kulkarni](https://twitter.com/kulkarniankita9)
- [Minko Gechev (@mgechev@mstdn.social)](https://twitter.com/mgechev)
- [Cory House](https://twitter.com/housecor)
- [Tomek Sułkowski](https://twitter.com/sulco)
- [Sebastien Lorber](https://twitter.com/sebastienlorber)
- [Steve (Builder.io)](https://twitter.com/Steve8708)
- [StackBlitz](https://twitter.com/StackBlitz)

## Author

👤 **Huynh Duc Dung**

- Website: https://productsway.com/
- Twitter: [@jellydn](https://twitter.com/jellydn)
- Github: [@jellydn](https://github.com/jellydn)

## Show your support

Give a ⭐️ if this project helped you!

[![kofi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/dunghd)
[![paypal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/dunghd)
[![buymeacoffee](https://img.shields.io/badge/Buy_Me_A_Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/dunghd)

## Stargazers

[![Stargazers repo roster for @jellydn/typescript-tips](https://reporoster.com/stars/jellydn/typescript-tips)](https://github.com/jellydn/typescript-tips/stargazers)

### Stargazers over time

[![Stargazers over time](https://starchart.cc/jellydn/typescript-tips.svg)](https://starchart.cc/jellydn/typescript-tips)
