<%*
    let rendermode = false;
    let type       = "";
    let pict       = "";
    let pict_width = 0;
    let scriptline = "";
    let firstline  = "";
    let sndline    = "";
    let thrdline   = "";
    let fourthline = "";
    let fifthline  = "";
    let prevlink   = "";
    let nextlink   = "";
    let lastline   = "";
    let fugger     = false; // used by example configurations


    let knownYAML  = ["cssclasses", "date_created", "publish", "tags", ];
    const inYAML   = new Map()
    let results    = await tp.user.foty(tp, app);

    if(results.CANCELLED == true) { return }

    for (const [key, value] of Object.entries(results)) {
        if(value == undefined) continue;
        if(key == "____") rendermode = true;
        if(rendermode) {
            if(value == "") continue;
            switch(key) {
                case "type":      type       = value; break;
                case "pict":      pict       = value; break;
                case "pict_width":pict_width = value; break;
                case "scriptline":scriptline = value; break;
                case "firstline": firstline  = value; break;
                case "sndline":   sndline    = value; break;
                case "thrdline":  thrdline   = value; break;
                case "fourthline":fourthline = value; break;
                case "fifthline": fifthline  = value; break;
                case "prevlink":  prevlink   = value; break;
                case "nextlink":  nextlink   = value; break;
                case "lastline":  lastline   = value; break;
                case "fugger":    fugger     = value; break;
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
    if(fugger && lastline != "") lastline="am ende "+type+"!";

    let value = ""
    let rend = ""
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
    if(scriptline != "") tR   += `${scriptline}\n`;
    if(pict!=""){
        if(pict_width!=0) {
            tR +=`![${pict_width}](${pict})`
        } else {
            tR +=`![](${pict})`
        }
        tR +=`\n`
    }
    if(firstline  != "") tR   += `# ${firstline}\n`;
    if(sndline    != "") tR += `${sndline}\n`;
    if(thrdline   != "") tR += `${thrdline}\n`;
    if(fourthline != "") tR += `${fourthline}\n`;
    if(fifthline  != "") rend += `${fifthline}\n`;
    if(nextlink!="") {
        if(prevlink!="") {
            rend += `&#9668;${prevlink}`
        }
        rend += `- ${nextlink}&#9658;\n`
    }
    if(lastline   != "") rend += `\n${lastline}\n`;
_%>
<% tp.file.cursor(1) _%>
<% rend _%>
