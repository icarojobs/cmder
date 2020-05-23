Acesse o seu C: e clone o repositório icarojobs/cmder. Em seguida siga os seguintes passos:

1. Adicione o caminho do Cmder.exe no path do SISTEMA:
C:\cmder;

2. Crie uma variável de SISTEMA chamada CMDER_ROOT com o seguinte valor:
C:\cmder

3. Execute o arquivo OpenCmderHere.reg

4. No visual studio code, adicione as seguintes configurações no settings.json:
"terminal.integrated.shell.windows": "C:\\Windows\\system32\\cmd.exe",
"terminal.integrated.shellArgs.windows": [
    "/k %CMDER_ROOT%\\vendor\\init.bat"
]

exemplo final do settings.json:
{
    "workbench.startupEditor": "newUntitledFile",
    "workbench.colorCustomizations": {},
    "terminal.integrated.automationShell.linux": "",

    "terminal.integrated.shell.windows": "C:\\Windows\\system32\\cmd.exe",
    "terminal.integrated.shellArgs.windows": [
        "/k %CMDER_ROOT%\\vendor\\init.bat"
    ]
}
