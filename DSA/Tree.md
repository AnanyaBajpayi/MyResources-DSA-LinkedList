### Tree
How to create a tree and traverse it using recursive inorder,preorder,postorder,levelorder
```c
struct node {
  int data;
  struct node *left;
  struct node *right;
};
struct node *newNode(int data) {
  struct node *node = (struct node *)malloc(sizeof(struct node));
  node->data = data;
  node->left = NULL;
  node->right = NULL;
  return (node);
}
// Traverse Preorder
void traversePreOrder(struct node *temp) {
  if (temp != NULL) {
    cout << " " << temp->data;
    traversePreOrder(temp->left);
    traversePreOrder(temp->right);
  }
}
// Traverse Inorder
void traverseInOrder(struct node *temp) {
  if (temp != NULL) {
    traverseInOrder(temp->left);
    cout << " " << temp->data;
    traverseInOrder(temp->right);
  }
}
// Traverse Postorder
void traversePostOrder(struct node *temp) {
  if (temp != NULL) {
    traversePostOrder(temp->left);
    traversePostOrder(temp->right);
    cout << " " << temp->data;
  }
}
//Traverse LevelOrder
vector<vector<int>> levelOrder(TreeNode* root) {
        vector<vector<int>> ans; 

        if(root == NULL) return ans; 

        queue<TreeNode*> q; 
        q.push(root); 

        while(!q.empty()) {
            int size = q.size();
            vector<int> level; 
            for(int i = 0;i<size;i++) {
                TreeNode *node = q.front(); 
                q.pop(); 
                if(node->left != NULL) q.push(node->left); 
                if(node->right != NULL) q.push(node->right); 
                level.push_back(node->val); 
            }

            ans.push_back(level); 
        }

        return ans; 
    }
int main() {
  struct node *root = newNode(1);
  root->left = newNode(2);
  root->right = newNode(3);
  root->left->left = newNode(4);

  cout << "preorder traversal: ";
  traversePreOrder(root);
  cout << "\nInorder traversal: ";
  traverseInOrder(root);
  cout << "\nPostorder traversal: ";
  traversePostOrder(root);
}
```

Iterative approach for preorder
```c
if(root==NULL)return v;
        stack<TreeNode*>st;
        st.push(root);
        while(!st.empty())
        {
            TreeNode* temp=st.top();
            st.pop();
            if(temp->right!=NULL)st.push(temp->right);
            if(temp->left!=NULL)st.push(temp->left);
            v.push_back(temp->val);
        }
```
Iterative approach for postorder
```c
if(root==NULL)return v;
        stack<TreeNode*>st;
        st.push(root);
        while(!st.empty())
        {
            TreeNode* temp=st.top();
            st.pop();
            if(temp->left!=NULL)st.push(temp->left);
            if(temp->right!=NULL)st.push(temp->right);
            v.push_back(temp->val);
        }
return reverse of v;
```
Iterative approach for inorder
```c
TreeNode* node=root;
      while(true)
      {
          if(node!=NULL)
          {
              st.push(node);
              node=node->left;
          }
          else
          {
              if(st.empty())break;
              TreeNode* temp=st.top();
              st.pop();
              v.push_back(temp->val);
              node=temp->right;
          }
      }
```

Iterative approach to do in ,pre ,post in one stack
```c
vector<int> postOrder(Node* node) {
        vector<int>pre;
        vector<int>in;
        vector<int>post;
        stack<pair<Node*,int>>st;
        if(node==NULL)return post;
        st.push({node,1});
        while(!st.empty())
        {
            auto it=st.top();
            st.pop();
            if(it.second==1)
            {
                pre.push_back(it.first->data);
                it.second++;
                st.push(it);
                if(it.first->left!=NULL)st.push({(it.first)->left,1});
            }
            else if(it.second==2)
            {
                in.push_back(it.first->data);
                it.second++;
                st.push(it);
                if(it.first->right!=NULL)st.push({(it.first)->right,1});
            }
            else
            {
                post.push_back(it.first->data);
            }
        }
        return post;
    }
```
