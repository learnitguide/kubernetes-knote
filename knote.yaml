---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: knote
spec:
  replicas: 1
  selector:
    matchLabels:
      app: knote
      tier: frontend
  template:
    metadata:
      labels:
        app: knote
        tier: frontend
    spec:
      containers:
        - name: app
          image: learnitguide/knotejs:1.0
          ports:
            - containerPort: 3000
          env:
            - name: MONGO_URL
              value: mongodb://mongo:27017/dev

---
apiVersion: v1
kind: Service
metadata:
  name: knote
spec:
  selector:
    app: knote
    tier: frontend

  ports:
    - port: 80
      targetPort: 3000
      nodePort: 30000
  type: NodePort
