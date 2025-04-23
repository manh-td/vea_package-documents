Usage of nossrfconst nossrf = require("nossrf")
const main = async()=>
{
    let is_safe =  await nossrf.asyncValidateUrl("https://google.com") // true means good
    if(is_safe){
        visitWebsiteWithoutRedirects("https://google.com")
    }
    is_safe =  await nossrf.asyncValidateUrl("file://etc/passwd") // false means malicious
    if(is_safe){ // this will not work because the is_safe is false
        visitWebsiteWithoutRedirects("file://etc/passwd")
    }
    console.log(await nossrf.asyncValidateUrl("http://192.168.1.1")) // false means malicious
    console.log(await nossrf.asyncValidateUrl("http://localhost/11")) // false means malicious

}
main()