# Addition-MultipicationMatrix
public class MatrixOpr 
 { 
  public static  Matrix add(Matrix mat,Matrix mat2) 
    {
  
     Matrix mat3 =new Matrix(mat.getNrow(),mat.getNcol());    
     for(int r=0;r<mat.getNrow();r++)
         {       
        for(int c=0;c<mat.getNcol();c++)              
            mat3.setElement(r,c, mat.getElement(r,c)+mat2.getElement(r,c));      
        }  
        return mat3;
     }
      public static  Matrix multiply(Matrix mat,Matrix mat2) 
  {  
      Matrix mat3 =new Matrix(mat.getNrow(),mat2.getNcol());            
      for(int r=0;r<mat.getNrow();r++) 
       {        
     for(int c=0;c<mat2.getNcol();c++)
      {
       double temp=0;  
       for(int r2=0;r2<mat2.getNrow();r2++)  
          temp += mat.getElement(r,r2)*mat2.getElement(r2,c);     
          mat3.setElement(r,c, temp);  
      }     
   }  
   return mat3;
 }
