<%*
    let autor      = "";
    let rendermode = false;
    let firstline  = "";
    let lastline   = "";


    let knownYAML  = ["autor" ];
    const inYAML   = new Map()
    let results    = await tp.user.poty(tp, app);

    if(results.CANCELLED == true) { return }

    for (const [key, value] of Object.entries(results)) {
        if(value == undefined) continue;
        if(key == "____") rendermode = true;
        if(rendermode) {
            if(value == "") continue;
            if(value == "!no!") continue;
            switch(key) {
                case "firstline": firstline  = value; break;
                case "lastline":  lastline   = value; break;
                default: break;
            }
        } else {
          if(value != "!no!") {
            inYAML.set(key,value);
          } else {
            let idx = knownYAML.indexOf(key);
            if (idx >= 0) {
              knownYAML.splice( idx, 1 );
            }
          }
        }
    }

    let value = ""
    let tE = ""
    tR += `---\n`;
    knownYAML.forEach(key => {
        value = inYAML.get(key)
        if(Array.isArray(value) && value.length > 1) {
            tR += `${key}: \n`;
            value.forEach((v,i) => {
                tR += `  - ${v}\n`;
            })
         } else {
            tR += `${key}: ${value}\n`;
         }
         inYAML.delete(key);
    })
    inYAML.forEach((val, key, m) => {
        if(Array.isArray(val)) {
            tR += `${key}: \n`;
            val.forEach((v,i) => {
                tR += `  - ${v}\n`;
            })
        } else {
            tR += `${key}: ${val}\n`;
        }
        inYAML.delete(key);
    })
    tR += `---\n`;
    if(firstline  != "") tR   += `${firstline}\n`;
    if(lastline   != "") tE   += `\n${lastline}\n`;
_%>
<% tp.file.cursor(1) _%>
<% tE _%>
 