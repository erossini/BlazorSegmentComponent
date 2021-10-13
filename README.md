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
![Blazor-Segmentation-example-blue](https://user-images.githubusercontent.com/9497415/137113256-9cc7d99f-4d3b-4914-894b-dfea51e4cc92.gif)

**Green**
![Blazor-Segmentation-example-green](https://user-images.githubusercontent.com/9497415/137113280-6ff0f8e7-9db4-4e9f-bf33-ba9bd72542e3.gif)

**Red**
![Blazor-Segmentation-example-red](https://user-images.githubusercontent.com/9497415/137113336-489abf47-ed40-461b-a8de-d2052924686e.gif)

**Light Colors**
![Blazor-Segmentation-example-lightcolors](https://user-images.githubusercontent.com/9497415/137113307-5ae60487-9e45-4f3e-9191-2e519ab2e3ba.gif)
