# Kosarkas#include <stdio.h>
int main ()
{
    int IdSvi[INT_MAX], PoeniMax = 0, IdMax = 0, PoeniMaxTmp, Kosarkas[3], i;
    while (true) {
        printf("Unesite ID kosarkasa:\n");
        scanf("%d", &Kosarkas[0]);
        printf("Unesite broj minuta:\n");
        scanf("%d", &Kosarkas[1]);
        printf("Unesite broj poena:\n");
        scanf("%d", &Kosarkas[2]);
        for(i = 0; i < sizeof(IdSvi); i++) {
            if(IdSvi[i] == Kosarkas[0]) {
                printf("Vec ste uneli kosarkasa sa ID-em %d\n", Kosarkas[0]);
                continue 2;
            }
        }
        if (Kosarkas[1] < 0 || Kosarkas[2] < 0) {
            break;
        }
        IdSvi(sizeOf(IdSvi)] = Kosarkas[0];
        PoeniMaxTmp = round((Kosarkas[2] / Kosarkas[1]) * 100) / 100;
        if (PoeniMaxTmp > PoeniMax) {
            PoeniMax = PoeniMaxTmp;
            IdMax = Kosarkas[0];
        }
    }
    printf("Najveci broj poena po minutu (%d) ima kosarkas sa ID-em %d\n", PoeniMax, IdMax);
}
