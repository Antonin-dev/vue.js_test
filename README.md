#Exo Vue with props

##use props for parent

_this.$emit("addTask", task)_</br> event for take props into parent</br></br>
_<Form @addTask="onAddTask"/>_</br>
Listen event into parent</br></br>
_Card :tasks="tasks"/>_ </br>
Send props to children
