# Archivos_bin
# parte del frame
package arbol_binario;

import javax.swing.tree.DefaultMutableTreeNode;
import javax.swing.tree.DefaultTreeModel;
import javax.swing.tree.TreePath;

/**
 *
 * @author paiz2
 */
public class frm_arbol_b extends javax.swing.JFrame {

    /**
     * Creates new form frm_arbol_b
     */
    String strRecorrido;
    public frm_arbol_b() {
        initComponents();
         txtConsola.setText("Programa iniciado correctamente..." + System.lineSeparator());
        
        btnLimpiarArbol.doClick();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jScrollPane1 = new javax.swing.JScrollPane();
        j_arbol = new javax.swing.JTree();
        btn_agregar = new javax.swing.JButton();
        txt_agregar = new javax.swing.JTextField();
        jScrollPane2 = new javax.swing.JScrollPane();
        txtConsola = new javax.swing.JTextArea();
        btnLimpiarArbol = new javax.swing.JButton();
        btn_Preorder = new javax.swing.JButton();
        btn_InOrder = new javax.swing.JButton();
        btn_PostOrder = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jScrollPane1.setViewportView(j_arbol);

        btn_agregar.setText("Agregar");
        btn_agregar.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btn_agregarActionPerformed(evt);
            }
        });

        txtConsola.setColumns(20);
        txtConsola.setRows(5);
        jScrollPane2.setViewportView(txtConsola);

        btnLimpiarArbol.setText("Limpiar");
        btnLimpiarArbol.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnLimpiarArbolActionPerformed(evt);
            }
        });

        btn_Preorder.setText("Preorder");
        btn_Preorder.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btn_PreorderActionPerformed(evt);
            }
        });

        btn_InOrder.setText("InOrder");
        btn_InOrder.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btn_InOrderActionPerformed(evt);
            }
        });

        btn_PostOrder.setText("PostOrder");
        btn_PostOrder.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btn_PostOrderActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jScrollPane1, javax.swing.GroupLayout.PREFERRED_SIZE, 212, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(layout.createSequentialGroup()
                                .addGap(44, 44, 44)
                                .addComponent(btnLimpiarArbol, javax.swing.GroupLayout.PREFERRED_SIZE, 150, javax.swing.GroupLayout.PREFERRED_SIZE))
                            .addGroup(layout.createSequentialGroup()
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jScrollPane2, javax.swing.GroupLayout.PREFERRED_SIZE, 312, javax.swing.GroupLayout.PREFERRED_SIZE)))
                        .addContainerGap(12, Short.MAX_VALUE))
                    .addGroup(layout.createSequentialGroup()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(layout.createSequentialGroup()
                                .addGap(46, 46, 46)
                                .addComponent(txt_agregar, javax.swing.GroupLayout.PREFERRED_SIZE, 108, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(btn_agregar))
                            .addGroup(layout.createSequentialGroup()
                                .addGap(98, 98, 98)
                                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                                    .addComponent(btn_PostOrder, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                    .addComponent(btn_InOrder, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                    .addComponent(btn_Preorder, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))))
                        .addGap(0, 0, Short.MAX_VALUE))))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(txt_agregar, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(btn_agregar))
                .addGap(18, 18, 18)
                .addComponent(btnLimpiarArbol)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(btn_Preorder)
                .addGap(18, 18, 18)
                .addComponent(btn_InOrder)
                .addGap(22, 22, 22)
                .addComponent(btn_PostOrder)
                .addGap(18, 18, 18)
                .addComponent(jScrollPane2, javax.swing.GroupLayout.PREFERRED_SIZE, 250, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(0, 14, Short.MAX_VALUE))
            .addGroup(layout.createSequentialGroup()
                .addGap(8, 8, 8)
                .addComponent(jScrollPane1)
                .addContainerGap())
        );

        pack();
    }// </editor-fold>                        

    private void btn_agregarActionPerformed(java.awt.event.ActionEvent evt) {                                            
        // TODO add your handling code here:
         try{
            
            if (txt_agregar.getText().length() <= 0) 
                    throw new Exception("¡Ingrese un valor por favor!");
                
            int valorNuevo = 0;
            try{ valorNuevo = Integer.parseInt(txt_agregar.getText());}
            catch(Exception ex){throw new Exception("¡Ingrese un entero!");}

            DefaultMutableTreeNode nodoRaiz = (DefaultMutableTreeNode) j_arbol.getModel().getRoot();
            if(nodoRaiz != null)
            {
                DefaultMutableTreeNode nodoAuxiliar = nodoRaiz;
                DefaultMutableTreeNode nodoPadre;
                
                while(true){
                    nodoPadre = nodoAuxiliar;
                    String s = nodoAuxiliar.getUserObject().toString().split("-")[1].trim();
                    int valorNodoActual = Integer.parseInt(s);
                    if(valorNuevo < valorNodoActual){
                        nodoAuxiliar = (DefaultMutableTreeNode) nodoAuxiliar.getFirstChild();
                        
                        if(nodoAuxiliar.getUserObject().toString().equals("I - NULL"))
                        {
                            nodoAuxiliar.setUserObject("I - " + valorNuevo);
                            nodoAuxiliar.add(new DefaultMutableTreeNode("I - NULL"));
                            nodoAuxiliar.add(new DefaultMutableTreeNode("D - NULL"));
                            
                            j_arbol.expandPath(new TreePath(nodoAuxiliar.getPath()));
                         txtConsola.setText(txtConsola.getText() + "Nuevo nodo agregado: " + txt_agregar.getText() + System.lineSeparator());
                            return;
                        }
                    }
                    else
                    {
                        nodoAuxiliar = (DefaultMutableTreeNode) nodoAuxiliar.getLastChild();
                        
                        if(nodoAuxiliar.getUserObject().toString().equals("D - NULL"))
                        {
                            nodoAuxiliar.setUserObject("D - " + valorNuevo);
                            nodoAuxiliar.add(new DefaultMutableTreeNode("I - NULL"));
                            nodoAuxiliar.add(new DefaultMutableTreeNode("D - NULL"));
                            
                            j_arbol.expandPath(new TreePath(nodoAuxiliar.getPath()));
                           txtConsola.setText(txtConsola.getText() + "Nuevo nodo agregado: " + txt_agregar.getText() + System.lineSeparator());
                            return;
                        }
                    }
                }
            }
            else {               
                              
                nodoRaiz = new DefaultMutableTreeNode("R - " + txt_agregar.getText());
                DefaultMutableTreeNode nodoIzquierdo = new DefaultMutableTreeNode("I - NULL");
                DefaultMutableTreeNode nodoDerecho = new DefaultMutableTreeNode("D - NULL");
                
                nodoRaiz.add(nodoIzquierdo);
                nodoRaiz.add(nodoDerecho);
                
                DefaultTreeModel modeloArbol = (DefaultTreeModel) j_arbol.getModel();
                modeloArbol.setRoot(nodoRaiz);
                
               txtConsola.setText(txtConsola.getText() + "Nodo RAÍZ agregado: " + txt_agregar.getText() + System.lineSeparator());
            }

        }catch(Exception ex)
        {
            txtConsola.setText(txtConsola.getText() + "Error en btnAgregarActionPerformed(): " + ex.getMessage() + System.lineSeparator());
        }          
    }                                           

    private void btnLimpiarArbolActionPerformed(java.awt.event.ActionEvent evt) {                                                
        try
        {
            DefaultTreeModel modeloArbol = (DefaultTreeModel) j_arbol.getModel();
            modeloArbol.setRoot(null);

            txtConsola.setText(txtConsola.getText() + "¡Vaciado del árbol! " + System.lineSeparator());
            txtConsola.setText("");
        }catch(Exception ex)
        {
            txtConsola.setText(txtConsola.getText() + "Error en btnLimpiarArbolActionPerformed(): " + ex.getMessage() + System.lineSeparator());
        }
    }                                               

    private void btn_PreorderActionPerformed(java.awt.event.ActionEvent evt) {                                             
        
    try{

      if(j_arbol.getModel().getRoot() == null)

      throw new Exception("¡Ningún nodo en el árbol para recorrer!");



      DefaultMutableTreeNode nodoRaiz = (DefaultMutableTreeNode) j_arbol.getModel().getRoot();

      txtConsola.setText(txtConsola.getText() + "Recorrido PREORDER: ");



      strRecorrido = "";

      RecorridoPreorder(nodoRaiz);

      txtConsola.setText(txtConsola.getText() + strRecorrido.substring(0, strRecorrido.length() - 3) + "." + System.lineSeparator());

    }catch(Exception ex)

    {

      txtConsola.setText(txtConsola.getText() + "Error en btnPreordenActionPerformed(): " + ex.getMessage() + System.lineSeparator());

    }
    }                                            

    private void btn_InOrderActionPerformed(java.awt.event.ActionEvent evt) {                                            
        try{

      if(j_arbol.getModel().getRoot() == null)

      throw new Exception("¡Ningún nodo en el árbol para recorrer!");



      DefaultMutableTreeNode nodoRaiz = (DefaultMutableTreeNode) j_arbol.getModel().getRoot();

      txtConsola.setText(txtConsola.getText() + "Recorrido INORDER: ");
      
      strRecorrido = "";
      
      RecorridoInorder(nodoRaiz);
      
        txtConsola.setText(txtConsola.getText() + strRecorrido.substring(0, strRecorrido.length() - 3) + "." + System.lineSeparator());
        }catch(Exception ex)

    {

      txtConsola.setText(txtConsola.getText() + "Error en btnPreordenActionPerformed(): " + ex.getMessage() + System.lineSeparator());

    }
    }                                           

    private void btn_PostOrderActionPerformed(java.awt.event.ActionEvent evt) {                                              
         try{

      if(j_arbol.getModel().getRoot() == null)

      throw new Exception("¡Ningún nodo en el árbol para recorrer!");



      DefaultMutableTreeNode nodoRaiz = (DefaultMutableTreeNode) j_arbol.getModel().getRoot();

      txtConsola.setText(txtConsola.getText() + "Recorrido POSTORDER: ");
      
      strRecorrido = "";
      
      RecorridoPostorder(nodoRaiz);
      
        txtConsola.setText(txtConsola.getText() + strRecorrido.substring(0, strRecorrido.length() - 3) + "." + System.lineSeparator());
        }catch(Exception ex)

    {

      txtConsola.setText(txtConsola.getText() + "Error en btnPreordenActionPerformed(): " + ex.getMessage() + System.lineSeparator());

    }
    }                                             

    
    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(frm_arbol_b.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(frm_arbol_b.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(frm_arbol_b.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(frm_arbol_b.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new frm_arbol_b().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton btnLimpiarArbol;
    private javax.swing.JButton btn_InOrder;
    private javax.swing.JButton btn_PostOrder;
    private javax.swing.JButton btn_Preorder;
    private javax.swing.JButton btn_agregar;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JScrollPane jScrollPane2;
    private javax.swing.JTree j_arbol;
    private javax.swing.JTextArea txtConsola;
    private javax.swing.JTextField txt_agregar;
    // End of variables declaration                   
    
//Metodo para Recorrido en Preornden
    public void RecorridoPreorder(DefaultMutableTreeNode nodoRaiz)

  {

    if(!nodoRaiz.getUserObject().toString().equals("I - NULL") && !nodoRaiz.getUserObject().toString().equals("D - NULL"))

    {

      strRecorrido += nodoRaiz.getUserObject().toString().split("-")[1].trim() + " - ";

      RecorridoPreorder((DefaultMutableTreeNode) nodoRaiz.getFirstChild());

      RecorridoPreorder((DefaultMutableTreeNode) nodoRaiz.getLastChild());

    }

  }
    
    //Metodo para Recorrido en Inornden
    private void RecorridoInorder(DefaultMutableTreeNode nodoRaiz) {
           if(!nodoRaiz.getUserObject().toString().equals("I - NULL") && !nodoRaiz.getUserObject().toString().equals("D - NULL"))

    {

      

      RecorridoInorder((DefaultMutableTreeNode) nodoRaiz.getFirstChild());
      
      strRecorrido += nodoRaiz.getUserObject().toString().split("-")[1].trim() + " - ";

      RecorridoInorder((DefaultMutableTreeNode) nodoRaiz.getLastChild());

    }

    }
//Metodo para Recorrido en Postornden
    private void RecorridoPostorder(DefaultMutableTreeNode nodoRaiz) {
             if(!nodoRaiz.getUserObject().toString().equals("I - NULL") && !nodoRaiz.getUserObject().toString().equals("D - NULL"))

    {

      RecorridoPostorder((DefaultMutableTreeNode) nodoRaiz.getFirstChild());
      RecorridoPostorder((DefaultMutableTreeNode) nodoRaiz.getLastChild());
      
      
      strRecorrido += nodoRaiz.getUserObject().toString().split("-")[1].trim() + " - ";
      
      

     

    }

    }
}


#Inserciones y recorridos del arbol 

package arbol_binario;

public class ArbolBinario {
    
    Nodo raiz;
    
    public ArbolBinario(){
        raiz = null;
    }
    
    public void insertar(int i, String contenido){
        Nodo n = new Nodo(i);
        n.valor = contenido;
        
        //INICIALIZANDO LA RAÍZ DEL ÁRBOL
        if(raiz == null)
            raiz = n;
        else{
            //RECORRIENDO EL ARBOL
            Nodo aux = raiz;
            while(aux != null){
                n.padre = aux;
                
                if(n.llave >= aux.llave)
                    aux = aux.derecha;
                else
                    aux = aux.izquierda;
            }
            
            //INSERCIÓN DEL NUEVO NODO
            if(n.llave < n.padre.llave)
                n.padre.izquierda = n;
            else
                n.padre.derecha = n;        
        }
    }
    
    public void recorrer(Nodo n){
        if(n != null)
        {
            recorrer(n.izquierda);
            System.out.println("Indice: " + n.llave + ", Valor: " + n.valor);
            recorrer(n.derecha);
        }
    }
 
    private class Nodo{
        public Nodo padre;
        public Nodo derecha;
        public Nodo izquierda;
        public int llave;
        public String valor;
        
        public Nodo(int indice){
            padre = null;
            derecha = null;
            izquierda = null;
            llave = indice;
            valor = null;
        }
    }
}

# Integrantes del grupo
0910-17-14985 Abner Saúl Marroquín Enríquez
0910-17-2822 Wilson Aldair Aguilar Samayoa
0910-12-17566 Christopher Alexander lemus Pereira
0910-18-2248 Pablo  Orlando Lopez Jimenez
Grupo No.5

