
//��ά����[[3,'*',6],['5.6','/',55],['12','*','d']]
// 3*6=18 '5.6'/55=NaN,'12'*'d'=NaN;  ���������� '��ĸ' * + - / '4'

    var b = [[30,'/',6],[100,'*',50],['5.6','/',55],['12','*','d'],['12','*','d'],[12,'*',7]];    //ĳ������
    var ss = []; //ѡ�������������ss[]��

    function Calculator(array) {
        if (!array || array.length <= 0) {
            return;
        }
        for (var i = 0; i < array.length; i++) {
            if (array[i] instanceof Array) {
                for (var j = 0; j < array[i].length; j++) {
                    ss.push(array[i][j]);
                }
            }
        }
        console.log(ss);
        for (var k = 0; k < ss.length; k++ ) {
            if (k % 3 === 0) {
                    if(typeof ss[k] ==='number' && typeof ss[k+2] ==='number') {
                        if(ss[ss+1]==='+') {
                            r = ss[k] + ss[k+2];
                            console.log(r);
                        } else if (ss[k+1]==='-') {
                            r = ss[k] - ss[k+2];
                            console.log(r);

                        } else if (ss[k+1]==='*') {
                            r = ss[k] * ss[k+2];
                            console.log(r);
                        } else if (ss[k+1]==='/') {
                            r = ss[k] / ss[k+2];
                            console.log(r);
                        }
                    }else {
                        console.log(NaN);
                    }
                 }

            }
    }
    Calculator(b);