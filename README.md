# NEW-HACK
Script roblox
local frame = script.Parent.Parent:WaitForChild("MainFrame")
local openButton = script.Parent
local passwordBox = frame:WaitForChild("PasswordTextBox")
local submitButton = frame:WaitForChild("SubmitButton")
local contentFrame = frame:WaitForChild("ContentFrame")

local CORRECT_PASSWORD = ">67<"

-- Inicialmente oculta el contenido hasta que se ingrese la contraseña
contentFrame.Visible = false

-- Función para alternar la visibilidad de la GUI principal
openButton.MouseButton1Click:Connect(function()
    frame.Visible = not frame.Visible
end)

-- Validar la contraseña
submitButton.MouseButton1Click:Connect(function()
    if passwordBox.Text == CORRECT_PASSWORD then
        contentFrame.Visible = true
        passwordBox.Text = ""
        passwordBox.PlaceholderText = "¡Acceso concedido!"
    else
        passwordBox.Text = ""
        passwordBox.PlaceholderText = "Contraseña incorrecta"
    end
end)
