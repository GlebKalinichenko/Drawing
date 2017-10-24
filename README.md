Node-Draw
=========

A multiplayer drawing application with touch support.

Uses: NodeJS, Socket.IO & HTML5 Canvas.

#Server

* io.sockets.on('connection', function (socket) {})
новое соединение

* socket.on('mousemove', function (data) {})
событие движения мыши по холсту

* socket.broadcast.emit('moving', data);
рассылка событий по всем подключенным клиентам


#Client

* function drawLine(fromx, fromy, tox, toy)
рисование линии

* canvas.on('touchstart', function(e) {})
событие для девайсов с тачпадом

* canvas.on('mouseup mouseleave', function(e) {})
мышь покинула холст - прекращаем рисовать

* canvas.on('touchend touchleave touchcancel', function(e) {})
клиент перестал взаимодествовать с тачпадом - прекращаем рисовать