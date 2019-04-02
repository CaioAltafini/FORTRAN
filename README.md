# Fortran
implicit none 
real p1, ma1, mb1, n1, p2, ma2, mb2, n2, qa, qf, mf, f

print *,"Digite as notas referente a N1(P1, MA1, MB1):"
read *, p1, ma1, mb1 

print *,"Digite as notas referente a N2(P2, MA2, MB2):"
read *, p2, ma2, mb2

print *, "Digite o valor referente a quantidade de aulas dadas e quantas aulas o aluno estava presente:"
read *, qa, qf

n1= (p1*0.7) + (ma1*0.2) + (mb1*0.1)
n2= (p2*0.7) + (ma2*0.2) + (mb2*0.1)

mf= (n1+(2*n2))/3

f= (qf*100)/qa

Print *, "Sua Situção é:"

if(f<75)then
print *,mf
print *,"Reprovado Por Falta"

else if(mf>5)then
print "(f0.2)",mf
print *,"Aprovado"

else if(mf>3 .and. mf<5)then
print *,mf
print *,"Recuperação"

else 
print *,mf
print *,"Reprovado Por Nota" 

endif
stop
end 
