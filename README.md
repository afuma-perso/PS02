export let count = (a: number[], b: number): number => {
    let c = 0;
    for (let n = 0; n < a.length; n++ ) {
        if (a[n] === b) {
            c++;
            n++;
            if (a[n] === b) {
                c++;
            }

        }
    }
    return c;
};
export let max = (d: number[]): number => {
    if (d.length === 0) {
    return Number.MIN_VALUE; 
    }
    let r = d[0];
    for (let q = 1; q < d.length; q++) {
        
        if (d[q] > r ) {
        r = d[q];
        }
    }
    return r;
    

 };
 export let has = (e:number[], f:number ): boolean => {
    for (let p = 0; p < e.length; p++) {
        if (f === e[p]) {
            return true;
        }
    } 
    return false;  
    
};
export let all = (g:number[], h:number ): boolean => {
    if (g.length === 0) {
        return false;
    }
    for (let s = 0; s < g.length; s++) {
        if (g[s] !== h) {
            return false;
        }
    }
    return true;
    
};
export let equals = (i:number[], j:number[]): boolean => {
    if (i.length === 0 && j.length === 0) {
        return true;
    }
    if (i.length !== j.length) {
        return false;
    }
    for (let t = 0; t < i.length; t++) {
        if (i[t] !== j[t]) {
            return false;
        }
    }
    return true;

};
export let cycle = (k:number, l:number): number[] => {
    let o: number[] = [];
    if (k <= 0 || l <= 0) {
        return [];
    }
    let n = 1;
    for (let m = 0; m < l; m++) {
        o[o.length] = n;
        if (n === k) {
            n = 1;
        } else {
            n++;
        }
    }
    return o;
};
export let concat = (u:number[], v:number[]): number[] => {
    let x: number[] = [];
    for (let w = 0; w < u.length; w++) {
        x[w] = u[w];
    }
    for (let w = u.length; w < (u.length + v.length); w++) {
        x[w] = v[w - u.length];
    }
    return x;
};
export let sub = (a:number[], b:number, c:number): number[] => {
    let d = [];
    if (c > a.length) {
        c = a.length;
    }
    if (b < 0) {
        b = 0;
    }
    for (let i = b; i < c; i++) {
        d[d.length] = a[i];

    }
    return d;
};
export let splice = (a:number[], b:number, c:number[]): number[] => {

    let f = [];
    if (b < 0) {
        return (concat (c, a));
    }
    if (b > a.length) {
        return (concat (a, c));
    }
    for (let i = 0; i < b; i++) {
        f[i] = a[i];
    }
    f = concat (f, c);
    for (let i = b; i < (a.length); i++) {
        f[f.length] = a[i];
    }
    return f;
};
