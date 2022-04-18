# TinyModules
A collection of tiny modules I have made

# Connections
A 18 line Signal/Event module

```lua
local Connection = Connections.new()

Connection:Connect(function(...)
    print(...)
end)

Connection:Fire("Hello", "World!")

Connection:Disconnect()
```

# Object
A 14 line Object-Oriented module

```lua
local Point = Object.new()

function Point:init(x, y)
    self.x = x
    self.y = y

    setmetatable(self, {
        __tostring = function(self)
            return string.format("(%d, %d)", self.x, self.y)
        end
    }

    return self
end

local p1 = Point.new(1, 2)

print(p1)
```
