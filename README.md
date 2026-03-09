# Xperience by Kentico Componennt Icons

[![Kentico Labs](https://img.shields.io/badge/Kentico_Labs-grey?labelColor=orange&logo=data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ic3ZnLWljb24iIHN0eWxlPSJ3aWR0aDogMWVtOyBoZWlnaHQ6IDFlbTt2ZXJ0aWNhbC1hbGlnbjogbWlkZGxlO2ZpbGw6IGN1cnJlbnRDb2xvcjtvdmVyZmxvdzogaGlkZGVuOyIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik05NTYuMjg4IDgwNC40OEw2NDAgMjc3LjQ0VjY0aDMyYzE3LjYgMCAzMi0xNC40IDMyLTMycy0xNC40LTMyLTMyLTMyaC0zMjBjLTE3LjYgMC0zMiAxNC40LTMyIDMyczE0LjQgMzIgMzIgMzJIMzg0djIxMy40NEw2Ny43MTIgODA0LjQ4Qy00LjczNiA5MjUuMTg0IDUxLjIgMTAyNCAxOTIgMTAyNGg2NDBjMTQwLjggMCAxOTYuNzM2LTk4Ljc1MiAxMjQuMjg4LTIxOS41MnpNMjQxLjAyNCA2NDBMNDQ4IDI5NS4wNFY2NGgxMjh2MjMxLjA0TDc4Mi45NzYgNjQwSDI0MS4wMjR6IiAgLz48L3N2Zz4=)](https://github.com/Kentico/.github/blob/main/SUPPORT.md#labs-limited-support) [![CI: Build and Test](https://github.com/Kentico/xperience-by-kentico-component-icons/actions/workflows/ci.yml/badge.svg)](https://github.com/Kentico/xperience-by-kentico-component-icons/actions/workflows/ci.yml)

[![Kentico.Xperience.ComponentIcons - NuGet Package](https://img.shields.io/nuget/v/Kentico.Xperience.ComponentIcons.svg)](https://www.nuget.org/packages/Kentico.Xperience.ComponentIcons)

## Description

A pre-packaged, annotated list of all icons used in Xperience by Kentico Page, Email, and Form Builder components. Great for AI agents building Xperience components!

The icon list is a C# class with doc comments on every icon that clearly describe what the icon looks like. This helps AI agents (and human developers) understand what the icon "looks like".

```csharp
public static class KenticoIcons
{
    /// <summary>
    /// Lowercase letter "a" in a simple font.
    /// </summary>
    public const string A_LOWERCASE = "icon-a-lowercase";
    /// <summary>
    /// Three horizontal lines with a bordered rectangle above.
    /// </summary>
    public const string ACCORDION = "icon-accordion";
    /// <summary>
    /// Puzzle piece with a plus sign circle badge.
    /// </summary>
    public const string ADD_MODULE = "icon-add-module";
    /// <summary>
    /// Simplified robot figure with antennae and rounded limbs.
    /// </summary>
    public const string ANDROID = "icon-android";
    /// <summary>
    /// Stylized apple with a leaf and a bite taken out
    /// </summary>
    public const string APPLE = "icon-apple";
    // ...
}
```

You can read about the inspiration for this library in the article [Smarter Components: Using Icon Metadata to Guide AI in Kentico Projects](https://community.kentico.com/blog/smarter-components-using-icon-metadata-to-guide-ai-in-kentico-projects).

## Requirements

### Library Version Matrix

This project has no dependencies and will work with any version of Xperience by Kentico.

### Dependencies

- [ASP.NET Core 10.0](https://dotnet.microsoft.com/en-us/download)
- [Xperience by Kentico](https://docs.kentico.com)

## Package Installation

Add the package to any project with component registration attributes, using the .NET CLI.

```powershell
dotnet add package Kentico.Xperience.ComponentIcons
```

## Quick Start

egister the library's services in your ASP.NET Core application:

```csharp
// FAQWidget.cs

using Kentico.Content.Web.Mvc;
using Kentico.PageBuilder.Web.Mvc;
using Kentico.Xperience.Admin.Base.FormAnnotations;
using Kentico.Xperience.Admin.Base.Forms;
using Kentico.Xperience.ComponentIcons;

[assembly: RegisterWidget(
    identifier: FAQWidget.IDENTIFIER,
    viewComponentType: typeof(FAQWidget),
    name: FAQWidget.NAME,
    propertiesType: typeof(FAQWidgetProperties),
    Description = "Displays FAQ items in an expandable accordion format",
    IconClass = KenticoIcons.CHECKLIST,
    AllowCache = true)]

namespace App.Components.PageBuilder.Widgets.FAQ;

public class FAQWidget : ViewComponent
{
  // ...
}
```

Every icon field in `KenticoIcons` is annotated with a comment describing the visual appearance of the icon. This means you can use an AI agent to select icons for each Widget, Section, etc... in your project by having it analyze the `KenticoIcons` class.

## Full Instructions

View the [Usage Guide](./docs/Usage-Guide.md) for more detailed instructions.

## Contributing

To see the guidelines for Contributing to Kentico open source software, please see [Kentico's `CONTRIBUTING.md`](https://github.com/Kentico/.github/blob/main/CONTRIBUTING.md) for more information and follow the [Kentico's `CODE_OF_CONDUCT`](https://github.com/Kentico/.github/blob/main/CODE_OF_CONDUCT.md).

Instructions and technical details for contributing to **this** project can be found in [Contributing Setup](./docs/Contributing-Setup.md).

## License

Distributed under the MIT License. See [`LICENSE.md`](./LICENSE.md) for more information.

## Support

[![Kentico Labs](https://img.shields.io/badge/Kentico_Labs-grey?labelColor=orange&logo=data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ic3ZnLWljb24iIHN0eWxlPSJ3aWR0aDogMWVtOyBoZWlnaHQ6IDFlbTt2ZXJ0aWNhbC1hbGlnbjogbWlkZGxlO2ZpbGw6IGN1cnJlbnRDb2xvcjtvdmVyZmxvdzogaGlkZGVuOyIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwYXRoIGQ9Ik05NTYuMjg4IDgwNC40OEw2NDAgMjc3LjQ0VjY0aDMyYzE3LjYgMCAzMi0xNC40IDMyLTMycy0xNC40LTMyLTMyLTMyaC0zMjBjLTE3LjYgMC0zMiAxNC40LTMyIDMyczE0LjQgMzIgMzIgMzJIMzg0djIxMy40NEw2Ny43MTIgODA0LjQ4Qy00LjczNiA5MjUuMTg0IDUxLjIgMTAyNCAxOTIgMTAyNGg2NDBjMTQwLjggMCAxOTYuNzM2LTk4Ljc1MiAxMjQuMjg4LTIxOS41MnpNMjQxLjAyNCA2NDBMNDQ4IDI5NS4wNFY2NGgxMjh2MjMxLjA0TDc4Mi45NzYgNjQwSDI0MS4wMjR6IiAgLz48L3N2Zz4=)](https://github.com/Kentico/.github/blob/main/SUPPORT.md#labs-limited-support)

This project has **Kentico Labs limited support**.

See [`SUPPORT.md`](https://github.com/Kentico/.github/blob/main/SUPPORT.md#full-support) for more information.

For any security issues see [`SECURITY.md`](https://github.com/Kentico/.github/blob/main/SECURITY.md).
