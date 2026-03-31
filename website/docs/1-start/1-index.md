# Introduction

- [Introduction](#introduction)
  - [Components](#components)

**Devotion** is a hybrid fullstack framework that - for now - allows to build _together_ a `Go` API, with maybe a `React`-based web client, and / or maybe a `React Native`-based Android / iOS app client.

So it basically helps developing and deploying this kind of setup:

```mermaid
flowchart
    api[Go API]:::clsApi
    api-. maybe used by .-> react[React web app]:::clsWeb
    api -. maybe used by .-> native["Android / iOS app <br>(via React Native)"]:::clsMob
    api -. maybe used by .-> other[Some other clients we're not developing ourselves]:::clsOther

    classDef clsApi fill:#000099,color:#fff;
    classDef clsWeb fill:#009900,color:#fff;
    classDef clsMob fill:#994433,color:#fff;
    classDef clsOther fill:#555555,color:#fff;
```

<br/>

:::info[Important info]
Devotion is made to work on **Unix**-based dev environments.
:::

:::warning
It might only partially work on Windows.
:::

<br/>

[top](#)

---

## Components

**Devotion** can be seen as 1 tool - [Aldev](../2-aldev/index.md) - and 5 libraries working together: [Goald](../3-goald/index.md), [GoaldR](../4-goaldr/index.md), [GoaldN](../5-goaldn/index.md), [CoreGo](../6-corego/index.md) and [CaroTS](../7-carots/index.md):

```mermaid
flowchart

    api[Go API]
    %% api-.-> react[React web app]
    %% api -.-> native["Android / iOS app <br>(via React Native)"]
    %% api -.-> other[Some other clients we're not developing ourselves]
    react[React web app]
    native["Android / iOS app <br>(via React Native)"]
    %% other[Some other clients we're not developing ourselves]

    CoreGo(["CoreGo <br >(library)"]):::clsApi -- is used to develop --> Goald & Aldev
    Goald(["Goald <br >(library)"]):::clsApi -- is used to develop --> api
    GoaldR(["GoaldR <br >(library)"]):::clsWeb -- is used to develop --> react
    GoaldN(["GoaldN <br >(library)"]):::clsMob -- is used to develop --> native
    CaroTS(["CaroTS <br >(library)"]):::clsWeb -- is used to develop --> GoaldR & GoaldN

    classDef clsApi fill:#000099,color:#fff;
    classDef clsWeb fill:#009900,color:#fff;
    classDef clsMob fill:#994433,color:#fff;
    classDef clsOther fill:#555555,color:#fff;
    classDef clsTool fill:#117799,color:#fff;

    Aldev{{Aldev}}:::clsTool
```

:::tip[As we'll see later on]
[Aldev](../2-aldev/index.md) is our special tool that helps build, locally and remotely deploy, test, and maintain both the libraries and the apps using them.
:::

<br/>

[top](#)

---
