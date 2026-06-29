# OS26 Liquid Glass Explorer(Default)

Author: [wasiabbas4pk](https://github.com/wasiabbas4pk)

This theme modifies key elements in the Windows 11 File Explorer to achieve a sleek, premium OS26 inspired Liquid Glass aesthetic with stylized elements.

## Explorer Previews
![preview-1](screenshot.png)

![preview-2](screenshot-2.png)


## Context Menu Previews
![Context-Menu-1](context-menu-1.png)

![Context-Menu-2](context-menu-2.png)

## Support for Light Mode

Unfortunately, this mod does not work appropriately with Light Mode. In Light Mode, the UI elements will not contrast with the background and the style won't look right.

## BlurBehind Requirements

To achieve the translucent effect in Explorer shown in the preview, you will need an external background blur tool:

* **Recommended:** The [Translucent Windows](https://windhawk.net/mods/translucent-windows) Windhawk mod (easiest to set up).
* **Alternative:** The third-party utility `ExplorerBlurMica`.

### Custom AccentBlurBehind Tinting
If the translucent background makes text hard to read on light backgrounds, you can add a custom AccentBlurBehind code in the settings page of the Translucent Windows Mod!
Here is a preview of the codes that can be used:

* **Tint Code 1:** `761E1E1E`

  Preview: 
  ![tint-1](tint-1.png) 

* **Tint Code 2:** `B31A1A1A`

  Preview: 
  ![tint-2](tint-2.png) 

* **Tint Code 3 (Default):** `3A232323`

  Preview:
  ![tint-3](tint-3.png) 

---

## Theme Selection
Once merged, this theme will be integrated natively into the mod configuration and can be toggled directly from the main dropdown menu in the mod settings.

## Manual Installation
To test or apply this theme manually right now:
1. Open the **Windows 11 File Explorer Styler** mod in Windhawk.
2. Navigate to the **Settings** tab and toggle the viewing mode to **"Textual mode"**.
3. Clear the text area, copy the complete configuration block below, paste it inside, and hit **"Save settings"**.

<details>
<summary> Content to import (click to expand)</summary>

```yaml
styleConstants:
  - ''
controlStyles:
  - target: Grid#DetailsViewControlRootGrid
    styles:
      - Margin=20,20,20,1
      - Background:=<WindhawkBlur BlurAmount="30" TintColor="#2D101010" TintOpacity="0.4"/>
      - CornerRadius=15

  - target: StackPanel#DetailsViewThumbnail > Grid
    styles:
      - Background=Transparent
  - target: Grid#HomeViewRootGrid
    styles:
      - Margin=20,20,20,0
      - Background:=<WindhawkBlur BlurAmount="30" TintColor="#2D101010" TintOpacity="0.4"/>
      - CornerRadius=15

  - target: FileExplorerExtensions.GalleryViewControl#GalleryViewControl > Grid
    styles:
      - Margin=20,20,20,0
      - Background:=<WindhawkBlur BlurAmount="30" TintColor="#2D101010" TintOpacity="0.4"/>
      - CornerRadius=15

  - target: Microsoft.UI.Xaml.Controls.Grid#GalleryRootGrid
    styles:
      - Margin=10
      - Background:=transparent
      - CornerRadius=15
  - target: Microsoft.UI.Xaml.Controls.AppBarButton > Grid@CommonStates
    styles:
      - Background@Disabled:=<WindhawkBlur BlurAmount="8" TintColor="#25ffffff"/>
 
      - CornerRadius@Disabled=12
      - BorderThickness@Disabled=1
      - Margin@Disabled=2,6,2,6
      - Padding@Disabled=0,-7
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>

  - target: Microsoft.UI.Xaml.Controls.AppBarButton#backButton > Grid@CommonStates
    styles:
      - Background@Disabled:=<WindhawkBlur BlurAmount="8" TintColor="#25ffffff"/>
      - CornerRadius@Disabled=11
      - BorderThickness@Disabled=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
      - Margin@Disabled=0,0,0,0
      - Height@Disabled=32
      - Width@Disabled=20
      - Padding@Disabled=0,-2,0,2
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#forwardButton > Grid@CommonStates
    styles:
      - Background@Disabled:=<WindhawkBlur BlurAmount="8" TintColor="#25ffffff"/>
      - CornerRadius@Disabled=11
      - BorderThickness@Disabled=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
      - Margin@Disabled=0,0,0,0
      - Height@Disabled=32
      - Width@Disabled=20
      - Padding@Disabled=0,-2,0,2
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#upButton > Grid@CommonStates
    styles:
      - Background@Disabled:=<WindhawkBlur BlurAmount="8" TintColor="#25ffffff"/>
      - CornerRadius@Disabled=11
      - BorderThickness@Disabled=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
      - Margin@Disabled=0,0,0,0
      - Height@Disabled=32
      - Width@Disabled=20
      - Padding@Disabled=0,-2,0,2
  - target: CommandBar#FileExplorerCommandBar
    styles:
      - Background=Transparent
      - HorizontalAlignment=1
  - target: CommandBar#FileExplorerSecondaryCommandBar
    styles:
      - Background=Transparent
      - MinHeight=0
  - target: Grid#TabContainerGrid > Border#LeftBottomBorderLine
    styles:
      - Visibility=Collapsed
  - target: Grid#TabContainerGrid > Border#RightBottomBorderLine
    styles:
      - Visibility=Collapsed
  - target: TabViewItem
    styles:
      - Margin=0,0,8,0
  - target: TabViewItem > Grid#LayoutRoot
    styles:
      - CornerRadius=12
      - Margin=2,4,0,4
      - Height=27
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - target: TabViewItem > Grid#LayoutRoot > Canvas
    styles:
      - Visibility=Collapsed
  - target: TabViewItem > Grid#LayoutRoot > Grid#TabContainer
    styles:
      - Background=Transparent
      - BorderThickness=0
  - target: TabViewItem > Grid#LayoutRoot@CommonStates
    styles:
      - Background@Selected:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - Background@PointerOverSelected:=<WindhawkBlur BlurAmount="15" TintColor="#35ffffff" />
      - Background@Normal:=<WindhawkBlur BlurAmount="15" TintColor="#15ffffff" />
  - target: Grid#TabContainerGrid > Border > Button#AddButton
    styles:
      - Visibility=Visible
      - Margin=0,0,0,2
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff"/>
      - CornerRadius=10
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush EndPoint="1,1" StartPoint="0,0"><GradientStop Color="#80ffffff" Offset="0.0"/><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55"/><GradientStop Color="#80ffffff" Offset="1"/></LinearGradientBrush>
      - Width=24
      - Height=24

  - target: Grid#CommandBarControlRootGrid
    styles:
      - Background=Transparent
  - target: Grid#NavigationBarControlGrid
    styles:
      - Background=Transparent
  - target: Microsoft.UI.Xaml.Controls.Grid#FileExplorerAddressBarGrid
    styles:
      - Margin=-6,0,0,0      
  - target: Grid#PART_LayoutRoot
    styles:
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - CornerRadius=14
      - BorderThickness=1
      - Margin=2
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - target: FileExplorerExtensions.CommandBarControl
    styles:
      - Margin=0,0,0,0
  - target: AutoSuggestBox#FileExplorerSearchBox > Grid#LayoutRoot > TextBox > Grid@CommonStates > Border#BorderElement
    styles:
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - CornerRadius=14
      - BorderThickness=1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - target: Microsoft.UI.Xaml.Controls.AppBarButton
    styles:
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - CornerRadius=12
      - BorderThickness=1
      - Margin=3,0,3,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - target: Microsoft.UI.Xaml.Controls.AppBarToggleButton
    styles:
      - Background:=<WindhawkBlur BlurAmount="15" TintColor="#25ffffff" />
      - CornerRadius=12
      - BorderThickness=1
      - Margin=3,0,3,1
      - BorderBrush:=<LinearGradientBrush StartPoint="0,0" EndPoint="1,1"><GradientStop Color="#80ffffff" Offset="0.0" /><GradientStop Color="{ThemeResource SurfaceStrokeColorDefault}" Offset="0.55" /><GradientStop Color="#80ffffff" Offset="1" /></LinearGradientBrush>
  - target: Microsoft.UI.Xaml.Controls.Grid#OuterOverflowContentRootV2
    styles:
      - CornerRadius=20
  - target: Button#MoreButton
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.AppBarSeparator
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#backButton
    styles:
      - Margin=0,9,9,0
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#forwardButton
    styles:
      - Margin=0,9,9,0
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#upButton
    styles:
      - Margin=0,9,9,0
  - target: Microsoft.UI.Xaml.Controls.AppBarButton#refreshButton
    styles:
      - Margin=0,9,9,0
themeResourceVariables:
  - ''
explorerFrameContainerHeight: 0
xamlDiagnosticsHandling: ''
