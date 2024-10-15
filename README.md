# Acrylic
This UI Library is skid

## Create Library
```lua
local Library = loadstring(game:HttpGetAsync('https://raw.githubusercontent.com/3345-c-a-t-s-u-s/Acrylic/refs/heads/main/source'))();
```

## Themes
Note: run this code before create window
```lua
Library.Theme:Default()
```
```lua
Library.Theme:Catppuccin()
```
```lua
Library.Theme:Neverlose()
```
```lua
Library.Theme:Dark()
```
```lua
Library.Theme:Light()
```
```lua
Library.Theme:Discord()
```
```lua
Library.Theme:Houston()
```
```lua
Library.Theme:Matcha()
```

## Create Window
```lua
local Window = Library:CreateWindow({
	Title = 'Acrylic',
	Logo = "rbxassetid://7733920644",
});
```

## Create Block
```lua
ExampleTab:AddBlock('Example')
```

## Create Button
```lua
ExampleTab:AddButton({
	Title = 'Button',
	Callback = function()
		print('Click!')
	end,
})
```

## Create Toggle
```lua
ExampleTab:AddToggle({
	Title = 'Toggle',
	Default = false,
	Callback = function(value)
		print('Toggle!',value)
	end,
})
```

## Create Slider
```lua
ExampleTab:AddSlider({
	Title = 'Slider',
	Max = 100,
	Min = 1,
	Default = 25,
	Round = 1,
	Callback = function(value)
		print('Slider!',value)
	end,
})
```

## Create Keybind
```lua
ExampleTab:AddKeybind({
	Title = 'Keybind',
	Default = "LeftControl",
	Callback = function(value)
		print('Keybind!',value)
	end,
})
```

## Create Textbox
```lua
ExampleTab:AddTextbox({
	Title = 'Textbox',
	PlaceHolder = 'Type something',
	--Default = "Text",
	Callback = function(value)
		print('Textbox!',value)
	end,
})
```

## Create Dropdown
```lua
ExampleTab:AddDropdown({
	Title = 'Dropdown',
	Values = {1,2,3,4,5,6,7,8,9,10},
	Default = 5,
	Callback = function(value)
		print('Dropdown!',value)
	end,
})
```

## Create Dropdown (Multiple)
```lua
ExampleTab:AddDropdown({
	Title = 'Multiple Dropdown',
	Values = {1,2,3,4,5,6,7,8,9,10},
	Default = {3,4,5,6,7},
	Multi = true,
	MaxMulti = 10,
	Callback = function(value)
		print('Multiple Dropdown!',value)
	end,
})
```

## Create Paragraph
```lua
ExampleTab:AddParagraph({
	Title = 'Paragraph',
	Description = "Description\n[1]: Example"
})
```

# Functions

### Disable Animation
```lua
Library.PerformanceMode = true;
```

### Change UI Size
```lua
Window:Resize(Library.SizeLibrary.Default) -- UDim2
```

# Example Code
```lua
local Library = loadstring(game:HttpGetAsync('https://raw.githubusercontent.com/3345-c-a-t-s-u-s/Acrylic/refs/heads/main/source'))();

Library.Theme:Discord()

local Window = Library:CreateWindow({
	Title = 'Acrylic',
	Logo = "rbxassetid://7733920644",
});

local ExampleTab = Window:AddTab({
	Title = 'Example',
	Icon = 'home',
});

local SettingsTab = Window:AddTab({
	Title = 'Settings',
	Icon = 'settings',
});

ExampleTab:AddBlock('Example')

ExampleTab:AddButton({
	Title = 'Button',
	Callback = function()
		print('Click!')
	end,
})

ExampleTab:AddToggle({
	Title = 'Toggle',
	Default = false,
	Callback = function(value)
		print('Toggle!',value)
	end,
})

ExampleTab:AddSlider({
	Title = 'Slider',
	Max = 100,
	Min = 1,
	Default = 25,
	Round = 1,
	Callback = function(value)
		print('Slider!',value)
	end,
})

ExampleTab:AddKeybind({
	Title = 'Keybind',
	Default = "LeftControl",
	Callback = function(value)
		print('Keybind!',value)
	end,
})


ExampleTab:AddTextbox({
	Title = 'Textbox',
	PlaceHolder = 'Type something',
	--Default = "Text",
	Callback = function(value)
		print('Textbox!',value)
	end,
})


ExampleTab:AddDropdown({
	Title = 'Dropdown',
	Values = {1,2,3,4,5,6,7,8,9,10},
	Default = 5,
	Callback = function(value)
		print('Dropdown!',value)
	end,
})

ExampleTab:AddDropdown({
	Title = 'Multiple Dropdown',
	Values = {1,2,3,4,5,6,7,8,9,10},
	Default = {3,4,5,6,7},
	Multi = true,
	MaxMulti = 10,
	Callback = function(value)
		print('Multiple Dropdown!',value)
	end,
})

ExampleTab:AddParagraph({
	Title = 'Paragraph',
	Description = "Device Supported:\n[Mobile]: ✅\n[PC]: ✅\n[Console]: ✅\n\nExecutor Supported:\nSolara\nZolara\nSynapse Z\nWave\nTrigon\nCode X\nArceus X\nFluxus\nSeliware"
})

SettingsTab:AddBlock('Settings')

SettingsTab:AddButton({
	Title = "Reset UI Size",
	Callback = function()
		Window:Resize(Library.SizeLibrary.Default)
	end,
})

SettingsTab:AddToggle({
	Title = 'Performance',
	Default = false,
	Callback = function(a)
		Library.PerformanceMode = a;
	end,
})

SettingsTab:AddBlock("")

SettingsTab:AddButton({
	Title = "Destroy UI",
	Callback = function()
		Window:Destroy()
	end,
})
```
