#Flexbox

##container
    display: flex

#####flex-direction
	row  
	row-reverse  
	column  
	column reverse 

#####flex-wrap
	nowrap (default)
	wrap (break to the next line)
	wrap reverse

#####justify-content
	flex-start (left)
	flex-end (right)
	center
	space-between
	space-around

#####align-items
	stretch (stretches element until the bottom, default)
	flex-start (align from top)
	flex-end (align from bottom)
	center
	baseline (align to the fontline)

#####align-content
	stretch (full height)
    flex-start (align from top)
	flex-end (align from bottom)
	center
	space-between
	space-around

##item
    order: -1 (before the other objects)
	order: 1 (after the other objects)
    flex-basis
    flex-grow
    flex-shrink
    flex
    align-self