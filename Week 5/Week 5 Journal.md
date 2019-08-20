# Week 5 Journal
## Session 1

### Request Object (Req)
https://googel.com/#q=express
http://www.yahoo.com/search?q=ali&first3
http://localhost:4200/home?test=1#history

Protocol
	* https:
Host 
	* Google.com, https://8.8.8.8
        * Sub-domain
            * www
Port 
    * local= 4200 
    * http = 80
    * https: = 443
    * ReactJS = 1023+ (Default = 3000)
Path
    localhost
        *Home
Querystring
    * ?q=ali&first3
    * ?test=1#history
                        (encoded uri)
Fragment/Hash(#)
    * #history

###HTTP Request methods
    * GET AND POST
Req Headers
    * 
    //shows header information in your browser
app.get(/headers, function(req, res){
    res.set('Content-Type', 'text/plain')
    var = s = ''
    for(var name in req.headers) s += ':' + req.header[name]
    res.send(s)
})
Req - instance of http request
    * req.params
    * req.query
    * req.body
    * req.route
    * req.headers

### Response Object (Res)
Starts as http service response

res.status
    * default = 200
    * Not found = 404
    * server error = 500
res.json() or res.json(status, json)
res.render (render page back)