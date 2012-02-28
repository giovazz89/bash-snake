About
---------------
A simple snake game written in Bash.


How to Play
---------------
Direction control: vim-style keys h, j, k and l;
Quit: q
Accept both upper- and lower-case.


Something to Say
---------------
 * Almisael has two processes, the foreground one responds to 
   user's control commands, the background one draws the board.

 * The snake is represented by the coordinate $head\_r and $head\_c indicating
   the row and column on which the snake head is, and a string $body which
   stores the directions from the head to tail. 
   e.g. a snake with this shape (@ is head):

        @
        oooo
           o

   will have a $body with value '21112', meaning 'down,right,right,right,down'

 * Use $! to grasp the PID of the latest created background process.

 * Use kill and trap to enable communication between the two processes.

 * When setting up several traps, it's necessary to guarantee that 
   the normal execution will not be interrupted by the signal handling 
   if the handlers envolve modification of some variables it depends on.
