#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.

;Wait for the error box
;	if the player is loaded ExitApp.
VPReady :=false
while VPReady=0
{
	; Error window
	IfWinExist, Microsoft Visual ahk_class #32770
	{
		WinActivate, Microsoft Visual ahk_class #32770
		GoSub HandleError
		break
	}	
}

;Quit the script if we're in the game or Visual pinball exited
GameReady :=false
while GameReady=0
{
	IfWinNotExist, Visual Pinball
		ExitApp
	
	IfWinExist, Visual Pinball Player
		ExitApp
}

;R6104 error box
HandleError:
IfWinExist, Microsoft Visual ahk_class #32770
{
	WinActivate, Microsoft Visual ahk_class #32770
	Send {Enter Down}{Enter Up}
	Sleep 1000 ; Sleepies? 
	IfWinExist, HD VGA PyProcGame ahk_class SDL_app
		GoSub PySDLToFront
    return
}
return

;SDL2 show on top
PySDLToFront:	
	WinWaitActive, HD VGA PyProcGame ahk_class SDL_app
	WinSet, AlwaysOnTop, On, HD VGA PyProcGame ahk_class SDL_app
	;WinActivate, Form1 ; B2S - PinballX should do this
	;WinActivate, Visual Pinball ; VP - PinballX should do this
return

