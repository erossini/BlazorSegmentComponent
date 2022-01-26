# Blazor Segment Component
This is a **Segment component** for [Blazor Web Assembly](https://www.puresourcecode.com/tag/blazor-webassembly/) and [Blazor Server](https://www.puresourcecode.com/tag/blazor-server/). The full explanation of the source code is on [PureSourceCode.com](https://www.puresourcecode.com/dotnet/blazor/segment-control-for-blazor/). Please leave your comment or question and use my [forum](https://www.puresourcecode.com/forum/). Please subscribe my [YouTube channel](https://www.youtube.com/channel/UC2jeteqpm3sUDqQpKGqpCLg?sub_confirmation=1).

## How to use it
First, add the NuGet package in your project. The name of the package is [PSC.Blazor.Components.Segments](https://www.nuget.org/packages/PSC.Blazor.Components.Segments/) and the only dependency it has is [Microsoft.AspNetCore.Components.Web](https://www.nuget.org/packages/Microsoft.AspNetCore.Components.Web/) (>= 5.0.10).

After that, in your `wwwroot\index.html` or in the `hosts` file, you have to add a theme (CSS) for your segment control. Obviously, you can create your own theme. So, use this code:

```
<link href="_content/PSC.Blazor.Components.Segments/themes/{theme-name}.css" rel="stylesheet" />
```

Out of the box, there are 4 themes (see below the images):

- Blue
- Green
- Red
- Light color

Then, in your `_Imports.razor` add this 

```
@using PSC.Blazor.Components.Segments
```

Now, you are ready to use your segment control.

## Example
As a user, I want to select a country from a list of countries. When I click on one of them, other data has to change accordingly.

So, in a page add the following code

```
<Segments OnSegmentChanged="OnSegmentChanged">
    <Segment Text="Global" Value="global"></Segment>
    <Segment Text="Australia" Value="australia"></Segment>
    <Segment Text="Brazil" Value="brazil"></Segment>
    <Segment Text="Canada" Value="canada"></Segment>
    <Segment Text="France" Value="france"></Segment>
    <Segment Text="Germany" Value="germany"></Segment>
    <Segment Text="Italy" Value="italy"></Segment>
    <Segment Text="Spain" Value="spain"></Segment>
    <Segment Text="UK" Value="uk"></Segment>
</Segments>
```

Each `Segment` has 2 properties:
- **Text**: the label you want to show to the user
- **Value**: the real value you want to use

The `Segments` has the property `OnSegmentChanged` that it is invoked every time a user click on a segment. So, define the function in your page the segment has to invoke like that

```
public async Task OnSegmentChanged(Segment segment)
{
    // code to run
}
```

## Themes 
There are 4 themes embedded in the segment control.

**Blue**
![Blazor-Segmentation-example-blue](https://user-images.githubusercontent.com/9497415/137144166-532c1055-1afa-47bf-8fcb-e0c5f988f86f.gif)

**Green**
![Blazor-Segmentation-example-green](https://user-images.githubusercontent.com/9497415/137144290-3684cae8-9730-4fb1-a3b4-894a7326b275.gif)

**Red**
![Blazor-Segmentation-example-red](https://user-images.githubusercontent.com/9497415/137144310-83b864eb-59e9-4dee-b73e-7eb3fd62fdae.gif)

**Light Colors**
![Blazor-Segmentation-example-lightcolors](https://user-images.githubusercontent.com/9497415/137144333-879efdc6-41b2-41b3-9e3a-ef73bf7a400b.gif)

---

## Other Blazor components

| Component name | Forum | Description |
|---|---|---|
| [DataTable for Blazor](https://www.puresourcecode.com/dotnet/net-core/datatable-component-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/forum/datatables/) | DataTable component for Blazor WebAssembly and Blazor Server |
| [Markdown editor for Blazor](https://www.puresourcecode.com/dotnet/blazor/markdown-editor-with-blazor/) | [Forum](https://www.puresourcecode.com/forum/forum/markdown-editor-for-blazor/) |  This is a Markdown Editor for use in Blazor. It contains a live preview as well as an embeded help guide for users. |
| [CodeSnipper for Blazor](https://www.puresourcecode.com/dotnet/blazor/code-snippet-component-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/codesnippet-for-blazor/) | Add code snippet in your Blazor pages for 196 programming languages with 243 styles |
| [Copy To Clipboard](https://www.puresourcecode.com/dotnet/blazor/copy-to-clipboard-component-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/copytoclipboard/) | Add a button to copy text in the clipbord | 
| SVG Icons and flags for Blazor | [Forum](https://www.puresourcecode.com/forum/icons-and-flags-for-blazor/) | Library with a lot of SVG icons and SVG flags to use in your Razor pages |
| [Modal dialog for Blazor](https://www.puresourcecode.com/dotnet/blazor/modal-dialog-component-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/forum/modal-dialog-for-blazor/) |  Simple Modal Dialog for Blazor WebAssembly |
| [PSC.Extensions](https://www.puresourcecode.com/dotnet/net-core/a-lot-of-functions-for-net5/) | [Forum](https://www.puresourcecode.com/forum/forum/psc-extensions/) |  A lot of functions for .NET5 in a NuGet package that you can download for free. We collected in this package functions for everyday work to help you with claim, strings, enums, date and time, expressions... |
| [Quill for Blazor](https://www.puresourcecode.com/dotnet/blazor/create-a-blazor-component-for-quill/) | [Forum](https://www.puresourcecode.com/forum/forum/quill-for-blazor/) |  Quill Component is a custom reusable control that allows us to easily consume Quill and place multiple instances of it on a single page in our Blazor application |
| [Segment for Blazor](https://www.puresourcecode.com/dotnet/blazor/segment-control-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/forum/segments-for-blazor/) |  This is a Segment component for Blazor Web Assembly and Blazor Server |
| [Tabs for Blazor](https://www.puresourcecode.com/dotnet/blazor/tabs-control-for-blazor/) | [Forum](https://www.puresourcecode.com/forum/forum/tabs-for-blazor/) |  This is a Tabs component for Blazor Web Assembly and Blazor Server |
| [WorldMap for Blazor]() | [Forum](https://www.puresourcecode.com/forum/worldmap-for-blazor/) | Show world maps with your data |

## More examples and documentation
*   [Write a reusable Blazor component](https://www.puresourcecode.com/dotnet/blazor/write-a-reusable-blazor-component/)
*   [Getting Started With C# And Blazor](https://www.puresourcecode.com/dotnet/net-core/getting-started-with-c-and-blazor/)
*   [Setting Up A Blazor WebAssembly Application](https://www.puresourcecode.com/dotnet/blazor/setting-up-a-blazor-webassembly-application/)
*   [Working With Blazor Component Model](https://www.puresourcecode.com/dotnet/blazor/working-with-blazors-component-model/)
*   [Secure Blazor WebAssembly With IdentityServer4](https://www.puresourcecode.com/dotnet/blazor/secure-blazor-webassembly-with-identityserver4/)
*   [Blazor Using HttpClient With Authentication](https://www.puresourcecode.com/dotnet/blazor/blazor-using-httpclient-with-authentication/)
*   [InputSelect component for enumerations in Blazor](https://www.puresourcecode.com/dotnet/blazor/inputselect-component-for-enumerations-in-blazor/)
*   [Use LocalStorage with Blazor WebAssembly](https://www.puresourcecode.com/dotnet/blazor/use-localstorage-with-blazor-webassembly/)
*   [Modal Dialog component for Blazor](https://www.puresourcecode.com/dotnet/blazor/modal-dialog-component-for-blazor/)
*   [Create Tooltip component for Blazor](https://www.puresourcecode.com/dotnet/blazor/create-tooltip-component-for-blazor/)
*   [Consume ASP.NET Core Razor components from Razor class libraries | Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/core/blazor/components/class-libraries?view=aspnetcore-5.0&tabs=visual-studio)
