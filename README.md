# miss1



   s(logical(tril(s,-1)))=2; %ispod glavne 
   
   a(logical(tril(ones(size(a)),-1)))= 'nesto' 
   
   a(logical(triu(a,1))) = 5 %iznad glavne
   
   a(logical(triu(ones(size(a)),1)))= 'nesto' 
   
   a(find(diag(diag(ones(size(a))))~=0)) = 5; %glavna
   
   a(logical(diag(diag(a)))) = 5; %glavna
   
   a(find(fliplr(diag(diag(ones(size(a)))))~=0)) = 5; %sporedna
   
     %-broj deljivih sa 3 u parnim kolonama

   s = a(:,2:2:end)
   s = s(mod(s,3)==0)
   s = length(s)
   
   % srednja vrednost mean()
   
   
   %primer plota 
   
   t=0:0.01:10;
   
  tp=rem(t,5);
  
  y=(tp<1)+(tp>=1 & tp<2).*(2-tp)+(tp>=2 & tp<3).*(1.5*tp-3)+...
  
  (tp>=3 & tp<4).*(6-1.5*tp)+(tp>=4 & tp<5)*0;
  
  plot(t,y);
