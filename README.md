# Packmac
IDEAL
MODEL small

STACK 100h
DATASEG
	x dw 1 dup (145, 146, 147, 148, 149, 150, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 140, 141, 142, 143, 144, 145, 146, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 145, 146, 147, 148, 149, 150)
	y dw 1 dup (80, 80, 80, 80, 80, 80, 81, 81, 81, 81, 81, 81, 81, 81, 81, 81, 82, 82, 82, 82, 82, 82, 82, 82, 82, 82, 82, 82, 83, 83, 83, 83, 83, 83, 83, 83, 83, 83, 83, 83, 83, 83, 84, 84, 84, 84, 84, 84, 84, 84, 84, 84, 84, 84, 84, 84, 85, 85, 85, 85, 85, 85, 85, 85, 85, 85, 85, 85, 85, 86, 86, 86, 86, 86, 86, 86, 86, 86, 86, 87, 87, 87, 87, 87, 87, 87, 88, 88, 88, 88, 88, 88, 88, 88, 88, 88, 89, 89, 89, 89, 89, 89, 89, 89, 89, 89, 89, 89, 89, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 90, 91, 91, 91, 91, 91, 91, 91, 91, 91, 91, 91, 91, 91, 91, 92, 92, 92, 92, 92, 92, 92, 92, 92, 92, 92, 92, 93, 93, 93, 93, 93, 93, 93, 93, 93, 93, 94, 94, 94, 94, 94, 94)
	color dw 165 dup (14)	
	
	upColliderX dw 1 dup (0,1,2,3,4,5,6,7,8,9,10,11,12,13,14) 
	upColliderY dw 1 dup (-1,-1,-1,-1,-1,-1,-1,-1,-1,-1,-1,-1,-1,-1,-1) 
	
	upColliderXoffset dw 15 dup(?)
	upColliderYoffset dw 15 dup(?)
	
	;pacmanUp dw 1 dup (3,4,10,11,2,3,4,10,11,12,1,2,3,4,5,9,10,11,12,13,1,2,3,4,5,9,10,11,12,130,1,2,3,4,5
	startingScreenMessage db "||| Welcome to PAC-MAN! |||",10,10,"Your goal is collect as many", 10, "points as you can",10,"before the ghost eats you",10,"For every dot you collect," , 10, "you get 1 point",10,"to win you need to eat all the points",10,10,"Controlls:",10,10," w-up, s-down a - left, d - right",10,10,"if you wish to start, click on a key -$"

	pacmanBlack dw 165 dup (0)
	PacmanXoffset dw 165 dup (?)
	PacmanYoffset dw 165 dup (?)
	 
	xoffset dw (?)
	yoffset dw (?)
	
	xoffsetNum dw (?)
	yoffsetNum dw (?)
	
	xRedGhost dw 1 dup  (56, 57, 58, 54, 55, 56, 57, 58, 59, 60, 53, 54, 55, 56, 57, 58, 59, 60, 61, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 51, 52, 54, 55, 58, 59, 60, 62, 63, 51, 55, 58, 59, 63)
	yRedGhost dw 1 dup (50, 50, 50, 51, 51, 51, 51, 51, 51, 51, 52, 52, 52, 52, 52, 52, 52, 52, 52, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 62, 62, 62, 62, 62, 62, 62, 62, 62, 63, 63, 63, 63, 63)
	colorRedGhost dw 1 dup (12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,15,15,12,12,12,15,15,12,12,12,15,15,54,54,12,15,15,54,54,12,12,15,15,54,54,12,15,15,54,54,12,12,12,15,15,15,15,12,15,15,15,15,12,12,12,12,12,15,15,12,12,12,15,15,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12,12)

	xPinkGhost dw 1 dup  (76, 77, 78, 74, 75, 76, 77, 78, 79, 80, 73, 74, 75, 76, 77, 78, 79, 80, 81, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 71, 72, 74, 75, 78, 79, 80, 82, 83, 71, 75, 78, 79, 83)
	yPinkGhost dw 1 dup (50, 50, 50, 51, 51, 51, 51, 51, 51, 51, 52, 52, 52, 52, 52, 52, 52, 52, 52, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 62, 62, 62, 62, 62, 62, 62, 62, 62, 63, 63, 63, 63, 63)
	colorPinkGhost dw 1 dup (60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,15,15,60,60,60,15,15,60,60,60,15,15,54,54,60,15,15,54,54,60,60,15,15,54,54,60,15,15,54,54,60,60,60,15,15,15,15,60,15,15,15,15,60,60,60,60,60,15,15,60,60,60,15,15,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60,60)

	xOrangeGhost dw 1 dup (116, 117, 118, 114, 115, 116, 117, 118, 119, 120, 113, 114, 115, 116, 117, 118, 119, 120, 121, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 111, 112, 114, 115, 118, 119, 120, 122, 123, 111, 115, 118, 119, 123)
	yOrangeGhost dw 1 dup (50, 50, 50, 51, 51, 51, 51, 51, 51, 51, 52, 52, 52, 52, 52, 52, 52, 52, 52, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 62, 62, 62, 62, 62, 62, 62, 62, 62, 63, 63, 63, 63, 63)
	colorOrangeGhost dw 1 dup (43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,15,15,43,43,43,15,15,43,43,43,15,15,54,54,43,15,15,54,54,43,43,15,15,54,54,43,15,15,54,54,43,43,43,15,15,15,15,43,15,15,15,15,43,43,43,43,43,15,15,43,43,43,15,15,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43,43)

	xBlueGhost dw 1 dup(96, 97, 98, 94, 95, 96, 97, 98, 99, 100, 93, 94, 95, 96, 97, 98, 99, 100, 101, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 91, 92, 94, 95, 98, 99, 100, 102, 103, 91, 95, 98, 99, 103)
	yBlueGhost dw 1 dup (50, 50, 50, 51, 51, 51, 51, 51, 51, 51, 52, 52, 52, 52, 52, 52, 52, 52, 52, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 53, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 54, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 55, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 56, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 57, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 58, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 59, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 60, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 61, 62, 62, 62, 62, 62, 62, 62, 62, 62, 63, 63, 63, 63, 63)
	colorBlueGhost dw 1 dup (11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,15,15,11,11,11,15,15,11,11,11,15,15,54,54,11,15,15,54,54,11,11,15,15,54,54,11,15,15,54,54,11,11,11,15,15,15,15,11,15,15,15,15,11,11,11,11,11,15,15,11,11,11,15,15,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11,11)
	
	collide dw 0
;--------------------------------------------------------------------------------------------------------------------------------
CODESEG


proc startScreen
	mov dx, offset startingScreenMessage
	mov ah,09h
	int 21h
	
	mov ah,0
	int 16h
	ret
endp startScreen


; fill screen with color
proc fillScreen
	push bp
	mov bp, sp
	push ax
	push cx
	push dx
	mov ax, [bp+4]
	mov ah, 0Ch
	mov cx, 320
	mov dx, 200

	rows:
	columns:
	int 10h
	loop columns
	dec dx
	cmp dx, 0
	jne rows

	pop dx
	pop cx
	pop ax
	pop bp
	ret 2
endp fillScreen
	
	
	;5 inputs fills a rectengular area with the color
	;1. x of first corner
	;2. y of first corner
	;3. x of second corner
	;4. y of second corner
	;5. color   

proc FillArea
	push ax
	push bx
	push cx
	push dx
	push bp
	mov bp, sp
	mov al,[bp+12]
	mov cx,200
	Area1:
		push cx
		dec cx
		cmp cx, [bp+18]
		jg yGreater
		cmp cx, [bp+14]
		jge yCorrect
		jmp yIncorrect
	yGreater:
		je yCorrect
		cmp cx,[bp+14]
		jle yCorrect
		jmp yIncorrect
	yCorrect:
		mov dx, cx
		mov cx, 320
		Area2:
			push cx
			dec cx
			cmp cx, [bp+20]
			je xCorrect
			jg xGreater
			cmp cx, [bp+16]
			jge xCorrect
			jmp xIncorrect
		xGreater:
			je xCorrect
			cmp cx,[bp+16]
			jle xCorrect
			jmp xIncorrect
		xCorrect:
			mov ah, 0Ch
			int 10h
		xIncorrect:
			pop cx
			loop Area2
	yIncorrect:
		pop cx
		loop Area1
		
	pop bp
	pop dx
	pop cx
	pop bx
	pop ax
	ret 10
endp FillArea

proc FillHEKEF
	push ax
	push bx
	push cx
	push dx
	push bp
	mov bp, sp
	mov al,[bp+12]
	mov cx,200
	Area_1:
	push cx
	dec cx
	cmp cx, [bp+18]
	jg y_Greater
	cmp cx, [bp+14]
	jge y_Correct
	jmp y_Incorrect
	y_Greater:
	je y_Correct
	cmp cx,[bp+14]
	jle y_Correct
	jmp y_Incorrect
	y_Correct:
	mov dx, cx
	mov cx, 320
	Area_2:
	push cx
	dec cx
	cmp cx, [bp+20]
	je x_Correct
	jg x_Greater
	cmp cx, [bp+16]
	jge x_Correct
	jmp x_Incorrect
	x_Greater:
	je x_Correct
	cmp cx,[bp+16]
	jle x_Correct
	jmp x_Incorrect
	x_Correct:
	cmp cx, [bp+16];abc
	je equal;abc
	cmp cx, [bp+20];abc
	je equal;abc
	cmp dx, [bp+18];abc
	je equal;abc
	cmp dx, [bp+14];abc
	je equal;abcabc
	jmp notEqual;abc
	equal:;abc
	mov ah, 0Ch
	int 10h
	notEqual:;abc
	x_Incorrect:
	pop cx
	loop Area_2
	y_Incorrect:
	pop cx
	loop Area_1
		
	pop bp
	pop dx
	pop cx
	pop bx
	pop ax
	ret 10
endp FillHEKEF

	
proc create
	push bp
	mov bp, sp
	push bx
	push cx
	push si
	mov cx, [bp+4]
	xor si, si
	
	printDotInArr:
	
	push cx
	mov bx, [bp+10]
	mov cx, [bx+si]
	mov bx, [bp+8]
	mov dx, [bx+si]
	mov bx, [bp+6]
	
	mov al, [byte ptr bx+si]
	mov ah, 0Ch
	int 10h
	
	pop cx
	add si, 2
	
	loop printDotInArr
	
	pop si
	pop cx
	pop bx
	pop bp
	ret 8
endp create

proc subNfromArray ;4 inputs 1.offset of original arr 2. offset of arr to save to 3. length of arrs 4. number to subtract
		;for every arr1[i] it save in arr2[i] = arr[i]-num
        push bp
        mov bp, sp
        push ax
		push bx
		push cx
		push dx
		mov bx, [bp + 10]
        mov dx, [bp + 8]
        mov cx, [bp + 6]
        mov al, [bp + 4]
    add_N:
            push bx
			push cx
			mov bl, [bx]
			sub bl, al
			mov cl, bl
			mov bx, dx
			mov [bx], cl
			pop cx
			pop bx
			add bx, 2
            add dx, 2
        loop add_N
        pop dx
		pop cx
		pop bx
		pop ax
		pop bp
		ret 8
endp subNfromArray



proc createFrame
	push 0
	call fillScreen
	
	push 10
	push 10
	push 310
	push 10
	push 3
	call fillArea
	
	push 10
	push 190
	push 310
	push 190
	push 3
	call fillArea
	
	push 10
	push 10
	push 10
	push 190
	push 3
	call fillArea
	
	push 310
	push 10
	push 310
	push 190
	push 3
	call fillArea
	
	push 15
	push 15
	push 305
	push 15
	push 3
	call fillArea

	push 15
	push 185
	push 305
	push 185
	push 3
	call fillArea
	
	push 15
	push 15
	push 15
	push 185
	push 3
	call fillArea
	
	push 305
	push 15
	push 305
	push 185
	push 3
	call fillArea
	ret
endp createFrame

proc Ghosts
; print all the ghosts
	push offset xRedGhost
	push offset yRedGhost
	push offset colorRedGhost
	push 144
	call create
	
	push offset xPinkGhost
	push offset yPinkGhost
	push offset colorPinkGhost
	push 144
	call create
	
	push offset xBlueGhost
	push offset yBlueGhost
	push offset colorBlueGhost
	push 144
	call create
	
	push offset xOrangeGhost
	push offset yOrangeGhost
	push offset colorOrangeGhost
	push 144
	call create
	ret
endp Ghosts

proc createBlocks
	push 33
	push 32
	push 75
	push 37
	push 3
	call FillHEKEF
	push 33
	push 32
	push 75
	push 32
	push 3
	call FillArea
	
	push 95
	push 32
	push 163
	push 37
	push 3
	call FillHEKEF
	push 95
	push 32
	push 163
	push 32
	push 3
	call FillArea
	
	push 181
	push 32
	push 224
	push 37
	push 3
	call FillHEKEF
	push 181
	push 32
	push 224
	push 32
	push 3
	call FillArea
	
	push 250
	push 32
	push 290
	push 37
	push 3
	call FillHEKEF
	push 250
	push 32
	push 290
	push 32
	push 3
	call FillArea
	
	push 240
	push 55
	push 290
	push 60
	push 3
	call FillHEKEF
	push 240
	push 55
	push 290
	push 55
	push 3
	call FillArea
	
	push 160
	push 60
	push 220
	push 65
	push 3
	call FillHEKEF
	push 160
	push 60
	push 220
	push 60
	push 3
	call FillArea
	
	push 100
	push 60
	push 115
	push 100
	push 3
	call FillHEKEF
	push 100
	push 60
	push 115
	push 60
	push 3
	call FillArea
	
	push 33
	push 60
	push 75
	push 65
	push 3
	call FillHEKEF
	push 33
	push 60
	push 75
	push 60
	push 3
	call FillArea
	ret
endp createBlocks

proc createBoard
	call createFrame
	call createBlocks
	ret
endp createBoard


proc collision ;checks if packman collided with something
	push ax
	push bx
	push cx	
	push dx
	push bp
	mov bp,sp
	mov cx, [bp+12]
	CollisionLoop:
		push cx
		mov bx, [bp+14]
		add bx, cx
		add bx, cx
		sub bx, 2
		mov dx, [bx]
		mov bx, [bp+16]
		add bx, cx
		add bx, cx
		sub bx,2
		mov cx, [bx]
		mov ah, 0Dh
		int 10h
		cmp al, 0
		je noCollison
		jmp collided
		noCollison:
		pop cx
		loop CollisionLoop
	pop bp
	pop dx
	pop cx
	pop bx
	pop ax
	ret 6
endp collision


start:

	mov ax, @data
	mov ds, ax
	mov ax,13h
	int 10h
	call startScreen
	
	push 0
	call fillScreen

	call createBoard
	

	
	LI:
	xor ax,ax
	mov ah, 0bh
	int 21h
	cmp al, 0FFh
	jne noPress
	
	mov ah, 7
	int 21h
	
	cmp al,87
	je upPress
	cmp al, 119
	je upPress
	
	cmp al, 68
	je rightPress
	cmp al, 100
	je rightPress
	
	cmp al, 83
	je downPress
	cmp al, 115
	je downPress
	
	cmp al, 65
	je leftPress
	cmp al, 97
	je leftPress
	
	jmp noPress
	
	upPress:
	mov [xoffsetNum], 0
	mov [yoffsetNum], 1
	jmp noPress
	
	rightPress:
	mov [xoffsetNum], 1
	mov [yoffsetNum], 0
	jmp noPress
	
	leftPress:
	mov [xoffsetNum], -1
	mov [yoffsetNum], 0
	jmp noPress
	
	downPress:
	mov [xoffsetNum], 0
	mov [yoffsetNum], -1
	jmp noPress
	
	noPress:
	push ax
	mov ax, [xoffsetNum]
	add [xoffset], ax
	mov ax, [yoffsetNum]
	add [yoffset], ax
	pop ax

	push offset PacmanXoffset
	push offset PacmanYoffset
	push offset pacmanBlack
	push 165  
	call create
	
	push offset x
	push offset PacmanXoffset
	push 165
	neg [xoffset]
	push [xoffset]
	call subNfromArray
	neg [xoffset]
	push offset y
	push offset PacmanYoffset
	push 165
	push [yoffset]
	call subNfromArray
	
	push offset PacmanXoffset
	push offset PacmanYoffset
	push 165
	call collision
	push offset PacmanXoffset
	push offset PacmanYoffset
	push offset color
	push 165  
	call create
	jmp cont
	
	collided:
	push ax
	mov ax, [xoffsetNum]
	sub [xoffset], ax
	mov ax, [yoffsetNum]
	sub [yoffset], ax
	pop ax
	push offset x
	push offset PacmanXoffset
	push 165
	neg [xoffset]
	push [xoffset]
	call subNfromArray
	neg [xoffset]
	push offset y
	push offset PacmanYoffset
	push 165
	push [yoffset]
	call subNfromArray
	push offset PacmanXoffset
	push offset PacmanYoffset
	push offset color
	push 165  
	call create
	
	cont:
	mov cx, 0
	mov dx, 08000h
	mov ah, 86h
	mov al, 0
	int 15h
	jmp LI
exit:
	mov ax, 4c00h
	int 21h
END start


